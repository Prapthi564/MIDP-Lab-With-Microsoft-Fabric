### Hands-On-Lab: Ingest data into the lakehouse

In this exercise, you ingest additional dimensional and fact tables from the Wide World Importers (WWI) into the lakehouse.

#### Task 3.1: Ingest data

1. Open/Navigate back to the **Fabric Workspace**, click on the **+ New** button and select **Data pipeline(Preview)**:

   ![new-data-pipeline](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/01.png?raw=true)

2. In the **New pipeline** dialog box, specify the name as **IngestDataFromSourceToLakehouse(1)** and select **Create(2)**. A new data factory pipeline is created and opened:

   ![name-data-pipeline](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/02.png?raw=true)

3. On your newly created data factory pipeline, select **Add pipeline activity(1)** to add an activity to the pipeline and select **Copy data(2)**. This action adds copy data activity to the pipeline canvas:

   ![add-pipeline-copy-data](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/03.png?raw=true)

4. Select the newly added copy data activity from the canvas. Activity properties appear in a pane below the canvas (you may need to expand the pane upwards by dragging the top edge). Under the **General(1)** tab in the properties pane, specify the name for the copy data activity **Data Copy to Lakehouse(2)**:

   ![name-copy-data](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/04.png?raw=true)

5. Navigate to the **Source(1)** tab of the selected copy data activity, select **External(2)** as Data store type and then select **+ New(3)** to create a new connection to data source:

   ![select-external-and-new](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/05.png?raw=true)

6. For this lab, all the sample data is available in a public container of Azure blob storage. You connect to this container to copy data from it. On the **New connection** wizard, select **Azure Blob Storage(1)** and then select **Continue(2)**:

   ![blob-continue](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/06.png?raw=true)

7. On the next screen of the **New connection** wizard, enter the following details and select Create to create the connection to the data source:

   - Account name or URI : **https://azuresynapsestorage.blob.core.windows.net/sampledata**
   - Connection	: **Create new connection**
   - Connection name:	**wwisampledata**
   - Authentication kind:	**Anonymous**

   ![create-connection](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/07.png?raw=true)

8. Once the new connection is created, specify the following properties before moving to the destination settings:

   - Data store type:**External**
   - Connection: **wwisampledata**
   - File path type:File path
   - File path	Container name (first text box): **sampledata**
   - Directory name (second text box): **WideWorldImportersDW/parquet**
   - Recursively	: Check this field
   - File Format	: **Binary**

   ![specify-details](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/08.png?raw=true)

9. Now, navigate to the **Destination(1)** tab of the selected copy data activity and specify the following properties:

  - Data store type: **Workspace**
  - Workspace data store type: **Lakehouse**
  - Lakehouse: **wwilakehouse**
  - Root Folder: **Files**
  - File path	Directory name (first text box): **wwi-raw-data**
  - File Format: **Binary**

    ![configure-destination](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/09.png?raw=true)

10. You have finished configuring the copy data activity. Select the **Save(1)** button on the top ribbon (under **Home**) to save your changes, and select **Run(2)** to execute your pipeline and its activity. This action triggers data copy from the underlying data source to the specified lakehouse and might take up to a minute to complete. You can monitor the execution of the pipeline and its activity under the **Output(3)** tab, which appears when you click anywhere on the canvas:

    ![run-pipeline](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/10.png?raw=true)

11. Now, navigate back to **Fabric workspace** and select **wwilakehouse** to launch **Lakehouse explorer**:

    ![launch-lakehouse-explorer](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/11.png?raw=true)

12. Validate that in the Lakehouse explorer view, a new folder **wwi-raw-data(1)** has been created and data for all the tables have been copied there:

    ![validate-all-data-has-been-copied](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/10/12.png?raw=true)

Congratulations! You have successfully learnt to ingest data into the lakehouse.

