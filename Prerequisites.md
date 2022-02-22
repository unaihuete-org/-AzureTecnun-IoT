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


In the Before the hands-on lab exercise, you will set up your environment for use in the rest of the hands-on lab. You should follow all the steps provided in the Before the hands-on lab section to prepare your environment **before attending** the hands-on lab. Failure to do so will significantly impact your ability to complete the lab within the time allowed.

> **IMPORTANT**: Most Azure resources require unique names. Throughout this lab you will see the word “SUFFIX” as part of resource names. You should replace this with your Microsoft alias, initials, or another value to ensure the resource is uniquely named.



### Task : Provision Power BI

If you do not already have a Power BI account:

1. Go to <https://powerbi.microsoft.com/features/>.

2. See the **What is Power BI** section of the page and select the **Start Free** button. Click on **Try Power BI for free**.

3. On the page, enter your provided Azure account (which should be the same account as the one you use for your Azure subscription), and select **Continue**.

4. Provide **Country** and **Phone Number**. Click on **Get Started** twice.
   > **Note**: You can always return to your Power BI environment by navigating to <https://app.powerbi.com/>.

### Task: Connect to your Lab VM

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

   - **Username**: `AdminTecnun`

   - **Password**: {check password in shared excel file}

7. Select **Yes** to connect, if prompted that the identity of the remote computer cannot be verified.

   ![In the Remote Desktop Connection dialog box, a warning states that the identity of the remote computer cannot be verified, and asks if you want to continue anyway. At the bottom, the Yes button is highlighted.](./media/remote-desktop-connection-identity-verification.png 'Remote Desktop Connection dialog')



You should follow all steps provided _before_ performing the Hands-on lab.
