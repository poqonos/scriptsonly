# HPE IMC Performance Perf Pack


This application primary goal is to add a performance pack in SCOM which get performance data from iMC using eAPI.

This performance pack use PowerShell script "SCOM_iMC_Perf_Integration_v0.3.ps1".

The SCOM performance pack itself (you can import in SCOM) is "perfiMC.integration.xml".

If you want to test the script without scom, you can run the script using the following syntax (and result will be exported in a txt or csv file):<BR>
&nbsp;&nbsp;&nbsp;&nbsp;SCOM_iMC_Perf_Integration_v0.3.ps1 &lt;type&gt; &lt;Device IP Address&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Where &lt;type&gt; is either csv or txt, and &lt;Device IP Address&gt; is an ip address of a device managed in iMC

Before trying the powershell script you have to modify iMC connexion parameters in the "# iMC Connection variable and initialization" section:<BR>
$imchost = "&lt;iMC IP Address&gt;"<BR>
$imcport = "&lt;iMC Port&gt;"<BR>
$imcprot = "&lt;http or https&gt;"<BR>
$iMCUser = "&lt;iMC user&gt;"<BR>
$iMCPWD = "&lt;iMC Password&gt;"

Also before importing SCOM management pack, you have to modify iMC connexion parameters in the "# iMC Connection variable and initialization" section of the xml file:<BR>
$imchost = "&lt;iMC IP Address&gt;"<BR>
$imcport = "&lt;iMC Port&gt;"<BR>
$imcprot = "&lt;http or https&gt;"<BR>
$iMCUser = "&lt;iMC user&gt;"<BR>
$iMCPWD = "&lt;iMC Password&gt;"<BR>

---------------------------------------------------------------------

New update 02-15-2016<BR>
---------------------------------------------------------------------

Found and correct an issue in the management pack for some systems ...
Added a new release (0.4) of the script (included in management pack) to also get bandwidth usage and un-reachability from iMC.
Also added some debug flags in the script.

----------------------------------------------------------------------

This sample app is provided under an Apache2 license. 

 Copyright 2016 Hewlett Packard Enterprise Development LP.

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.