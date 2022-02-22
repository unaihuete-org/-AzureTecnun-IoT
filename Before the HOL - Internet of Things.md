![Microsoft Cloud Workshops](https://github.com/Microsoft/MCW-Template-Cloud-Workshop/raw/main/Media/ms-cloud-workshop.png 'Microsoft Cloud Workshops')

<div class="MCWHeader1">
Internet of Things
</div>

<div class="MCWHeader2">
Before the hands-on lab setup guide
</div>

<div class="MCWHeader3">
October 2021
</div>

Information in this document, including URL and other Internet Web site references, is subject to change without notice. Unless otherwise noted, the example companies, organizations, products, domain names, e-mail addresses, logos, people, places, and events depicted herein are fictitious, and no association with any real company, organization, product, domain name, e-mail address, logo, person, place or event is intended or should be inferred. Complying with all applicable copyright laws is the responsibility of the user. Without limiting the rights under copyright, no part of this document may be reproduced, stored in or introduced into a retrieval system, or transmitted in any form or by any means (electronic, mechanical, photocopying, recording, or otherwise), or for any purpose, without the express written permission of Microsoft Corporation.

Microsoft may have patents, patent applications, trademarks, copyrights, or other intellectual property rights covering subject matter in this document. Except as expressly provided in any written license agreement from Microsoft, the furnishing of this document does not give you any license to these patents, trademarks, copyrights, or other intellectual property.

The names of manufacturers, products, or URLs are provided for informational purposes only and Microsoft makes no representations and warranties, either expressed, implied, or statutory, regarding these manufacturers or the use of the products with any Microsoft technologies. The inclusion of a manufacturer or product does not imply endorsement of Microsoft of the manufacturer or product. Links may be provided to third party sites. Such sites are not under the control of Microsoft and Microsoft is not responsible for the contents of any linked site or any link contained in a linked site, or any changes or updates to such sites. Microsoft is not responsible for webcasting or any other form of transmission received from any linked site. Microsoft is providing these links to you only as a convenience, and the inclusion of any link does not imply endorsement of Microsoft of the site or the products contained therein.

© 2021 Microsoft Corporation. All rights reserved.

Microsoft and the trademarks listed at <https://www.microsoft.com/en-us/legal/intellectualproperty/Trademarks/Usage/General.aspx> are trademarks of the Microsoft group of companies. All other trademarks are property of their respective owners.

**Contents**

<!-- TOC -->

- [Internet of Things before the hands-on lab setup guide](#internet-of-things-before-the-hands-on-lab-setup-guide)
  - [Requirements](#requirements)
  - [Before the hands-on lab](#before-the-hands-on-lab)
    - [Task 1: Provision a resource group](#task-1-provision-a-resource-group)
    - [Task 2: Setup a lab virtual machine](#task-2-setup-a-lab-virtual-machine)
    - [Task 3: Provision Azure Databricks](#task-3-provision-azure-databricks)
    - [Task 4: Create Databricks cluster](#task-4-create-databricks-cluster)
    - [Task 5: Provision Power BI](#task-5-provision-power-bi)
    - [Task 6: Connect to your Lab VM](#task-6-connect-to-your-lab-vm)
    - [Task 7: Download Google Chrome](#task-7-download-google-chrome)
    - [Task 8: Download Smart Meter Simulator project](#task-8-download-smart-meter-simulator-project)

<!-- /TOC -->

# Internet of Things before the hands-on lab setup guide

## Requirements

- Microsoft Azure subscription must be pay-as-you-go or MSDN.
  - Trial subscriptions will not work.
- A virtual machine configured with:
  - Visual Studio Community 2019 or later
  - Azure SDK 2.9 or later (Included with Visual Studio)
- A running Azure Databricks cluster.
- A work email address that has Power BI enabled, allowing you to create a Power BI account if one does not exist.

## Before the hands-on lab

Duration: 45 minutes

In the Before the hands-on lab exercise, you will set up your environment for use in the rest of the hands-on lab. You should follow all the steps provided in the Before the hands-on lab section to prepare your environment **before attending** the hands-on lab. Failure to do so will significantly impact your ability to complete the lab within the time allowed.

> **IMPORTANT**: Most Azure resources require unique names. Throughout this lab you will see the word “SUFFIX” as part of resource names. You should replace this with your Microsoft alias, initials, or another value to ensure the resource is uniquely named.



### Task 5: Provision Power BI

If you do not already have a Power BI account:

1. Go to <https://powerbi.microsoft.com/features/>.

2. See the **What is Power BI** section of the page and select the **Start Free** button. Click on **Try Power BI for free**.

3. On the page, enter your provided Azure account (which should be the same account as the one you use for your Azure subscription), and select **Continue**.

4. Provide **Country** and **Phone Number**. Click on **Get Started** twice.
   > **Note**: You can always return to your Power BI environment by navigating to <https://app.powerbi.com/>.

### Task 6: Connect to your Lab VM

In this task, you will create an RDP connection to your lab virtual machine (VM).

1. In the [Azure portal](https://portal.azure.com), open your resource group named `hands-on-lab-SUFFIX`.

2. In the list of resources for your resource group, select the **LabVM** virtual machine.

   ![The list of resources in the hands-on-lab-SUFFIX resource group are displayed, and LabVM is highlighted.](./media/resource-group-resources-labvm.png 'LabVM in resource group list')

3. On your **LabVM** resource screen, expand **Connect** from the top menu, and select RDP.

   ![The LabVM resource screen is displayed, with the Connect button highlighted in the top menu.](./media/connect-labvm.png 'Connect to LabVM')

4. Select **Download RDP file**, then open the downloaded RDP file.

   ![The Connect screen is displayed and the Download RDP file button is highlighted.](./media/connect-to-virtual-machine.png 'Connect to virtual machine')

5. Select **Connect** on the **Remote Desktop Connection** dialog.

   ![In the Remote Desktop Connection Dialog Box, the Connect button is highlighted.](./media/remote-desktop-connection.png 'Remote Desktop Connection dialog')

6. Enter the following credentials when prompted:

   - **Username**: `demouser`

   - **Password**: {Your password}

7. Select **Yes** to connect, if prompted that the identity of the remote computer cannot be verified.

   ![In the Remote Desktop Connection dialog box, a warning states that the identity of the remote computer cannot be verified, and asks if you want to continue anyway. At the bottom, the Yes button is highlighted.](./media/remote-desktop-connection-identity-verification.png 'Remote Desktop Connection dialog')

8. Once logged in, launch the **Server Manager**. This should start automatically, but you can access it via the Start menu if it does not start.

   ![The Server Manager tile is circled in the Start Menu.](./media/start-menu-server-manager.png 'Server Manager tile in the Start menu')

9. Select **Local Server**, then select **On** next to **IE Enhanced Security Configuration**. **Note:** If the link says `Off`, skip ahead to the next task.

   ![Screenshot of the Server Manager. In the left pane, Local Server is selected. In the right, Properties (For LabVM) pane, the IE Enhanced Security Configuration, which is set to On, is highlighted.](./media/windows-server-manager-ie-enhanced-security-configuration.png 'Server Manager')

10. In the **Internet Explorer Enhanced Security Configuration** dialog, select **Off** under **Administrators**, then select **OK**.

    ![Screenshot of the Internet Explorer Enhanced Security Configuration dialog box, with Administrators set to Off.](./media/internet-explorer-enhanced-security-configuration-dialog.png 'Internet Explorer Enhanced Security Configuration dialog box')

11. Close the **Server Manager**.


### Task 8: Download Smart Meter Simulator project

Fabrikam has provided a Smart Meter Simulator that they use to simulate device registration, as well as the generation and transmission of telemetry data. They have asked you to use this as the starting point for integrating their smart meters with Azure.

1. From your **LabVM**, download the starter project by downloading a .zip copy of the Internet of Things MCW GitHub repo.

2. In your newly installed Chrome web browser, navigate to the Internet of Things MCW repo: <https://github.com/Microsoft/MCW-Internet-of-Things>.

3. On the repo page, expand the **Code** button, then select **Download ZIP**.

   ![Download .zip containing the Internet of Things MCW repository](media/git-hub-download-repo.png 'Download ZIP')

4. Unzip the contents to the folder **C:\SmartMeter**.

5. Navigate to the `SmartMeterSimulator.sln` file within the `Hands-on lab\lab-files\starter-project` folder and open it with **Visual Studio 2019**.

6. Sign into Visual Studio or create an account, if prompted.

7. If the Security Warning for SmartMeterSimulator window appears, un-check **Ask me for every project in this solution** and select **OK**.

   ![The SmartMeterSimulator Security Warning window has the option to "Ask me for every project in this solution" highlighted.](./media/visual-studio-security-warning.png 'SmartMeterSimulator Security Warning')

> **Note**: If you attempt to build the solution at this point, you will see many build errors. This is intentional. You will correct these in the exercises that follow.

You should follow all steps provided _before_ performing the Hands-on lab.
