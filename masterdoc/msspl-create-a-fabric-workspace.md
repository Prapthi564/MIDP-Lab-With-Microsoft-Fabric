### Hands-On-Lab: Create a Fabric workspace

In this exercise, you build a lakehouse, ingest sample data into the delta table, apply transformation where required, and then create reports.

#### Task 1.1: Assign Fabric Administrator Role

1. Start by searching for **Azure Active Directory** in the search pane in Azure portal:

   ![Navigate-To-AAD](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/01.png?raw=true)

2. Navigate to **Roles and administrators**:

   ![Roles-and-Administrator](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/02.png?raw=true)

3. In the **Roles and administrators** page, search for **Fabric Administrator**, and click on it:

   ![search-fabric-admin](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/03.png?raw=true)

4. This will take you to the **Fabric Administrator | Assignments** page where you will have to assign yourself the **Fabric Administrator role**. Now, click on **+ Add Assignments**:

   ![click-add-assignments](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/04.png?raw=true)

5. Make sure to **check the box(1)** next to your username, confirm if it is **Selected(2)** and click on **Add(3)**:

   ![check-and-add-role](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/05.png?raw=true)

6. You can confirm the **Fabric Administrator** role has been added successfully by **refreshing(1)** Fabric Administrators | Assignments page. After **confirming(2)** it has been added successfully, navigate back to **Home(3)**.

   ![check-and-navigate-back-to-home](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/06.png?raw=true)

----

#### Task 1.2: Sign up for Microsoft Fabric Trial

1. Copy the **Power BI homepage link**, and open this link inside the VM in a new tab:

   ```
   https://powerbi.com
   ```

2. Select **Account manager(1)**, and click on **Start trial(2)**:

   ![Account-manager-start](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/07.png?raw=true)

3. A new prompt will appear asking you to **Upgrade to a free Microsoft Fabric trial**, click on **Start trial(1)**:

   ![Start-trial](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/08.png?raw=true)

4. Once your trial capacity is ready, you receive a confirmation message. Select **Got it(1)** to begin working in Fabric:

   ![Got-it](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/09.png?raw=true)

6. Now, open **Account manager(1)** again, and verify **Trial status(2)**.

   ![Verify-trial-status](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/10.png?raw=true)

----

#### Task 1.3: Create a workspace

Here, you create a Fabric workspace. The workspace contains all the items needed for this lakehouse tutorial, which includes lakehouse, dataflows, Data Factory pipelines, the notebooks, Power BI datasets, and reports.

1.  Now, select **Workspaces** and click on **+ New workspace**:

    ![New Workspace](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/11.png?raw=true)

2. Fill out the **Create a workspace** form with the following details:

   - **Name:** Enter **Fabric Lakehouse Tutorial**, and any extra characters to make the name unique.
   - **Description:** Lakehouse Demo

   ![name-and-desc-of-workspc](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/12.png?raw=true)

   - **Advanced:** Expand it and Under **License mode**, select **Trial capacity(1)**.

3. Select on **Apply(2)** to create and open the workspace.

   ![advanced-and-apply](https://github.com/CloudLabsAI-Azure/MIDP-Lab-With-Microsoft-Fabric/blob/dev/media/08/13.png?raw=true)

Congratulations! You have successfully learnt to create a Fabric workspace.

