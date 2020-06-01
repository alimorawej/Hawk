
# <img src="../Hawk.png" width="134" height="75"> Appendix II

### Case Study A: Engineering level - Customer Claim Analysis.

<p> Throughout this case study it is assumed that a complaint is recorded by the user and that after initial filtering the complaint is passed to the responsible engineer for further investigation. Without Hawk looking for all the necessary information for trouble shooting is a time consuming task. Plus as the mobile networks get more crowded with new nodes,  the collection of the relevant data in a presentable format, will take a considerable amount of time .The consulting software Hawk could considerably save this time by searching the available data and providing it in a format that would be much time efficient for the engineer. In addition, with the help of Artificial Intelligence Hawk gives smart hints and suggestions.  In time, then Hawk looks into more cases to learn from them.</p>
<p>Below are typical process (Streisand of data) that is used for solving the case of reported complaint by a user of a mobile operator.</p>

#### Step 1. CRM analysis and filtering - Identifying physical location of the problem area.

<p>The first step is to Geographically isolate the problematic area. In order to identify where the potential cells for establishing the wireless connection are, the engineer needs the exact physical location of the failure. This can be done by GPS information of the failure, or the address of the failure, next the site that was the main link of the connection. This may come from the identification information of the cell that is on the broadcast channel or can be estimated by considering the closest site to the failure location (the best cell). So it is useful for trouble shooting to have the information regarding the main neighbors of the failure site. Any failure on the neighboring cells could affect the call. The information on the sites that are overshooting to the area of the failure (hence are contributing to the interference) also can be useful source of information.</p>
<p><b>Hawk</b> will look at the GPS information or the address from the complaint record as well as the cell identification information on the link to pinpoint the geographical information of the user during the fault and the location of the serving cell on the map.</p>

#### Step 2. Checking the user profile in HSS. 

<p>The kind of limitation that has been set for the customer by the operator is recorded in HSS. For example if the customer is complaining that the service he or she is receiving is not more than 10 MBPS there is a possibility that this limit has already been defined for the customer by the service provider (The Operator).</p>  
<p><b>Hawk</b> will check and provide the limitations that the service provider has put for the user.</p>

#### Step 3. CRM and CDR correlation - Potential problematic cell sites and user location. 

<p>CRM and CDR are two independent sources of information that can be looked into independently. Comparing and correlating them will provide useful hints in narrowing down the problem. The CRM contains records based on observation of the issue according to the user of the service and CDR contains the information regarding the specific call or Data session that has an issue recoded by the network’s main switch center. CDR and CRM should be compared for the engineer to identify the cell and channels that were last used by the customer at the time of the fault. For example does the location information on the CRM confirms the cell information on CDR. Is the user at the time of issue fault connected to the cell that is closest to it? And if not is there a good reason for it?.</p>
<p><b>Hawk</b> will initially search and pull out the appropriate CRM and CDR and decides whether the connection of the user during the assurance of the problem was connected to the nearest site or not and if not was there an issue on the nearest site that forced the link on an alternate cell.</p>

#### Step 4. Identifying serving cells and neighboring cells.

<p>Next for further investigation the engineer needs to look into the defined neighbor cells in the network for any signs of problem. 
Hawk will list the neighbor cells including and signs of fault that was recorded during the reported fault. (Vital KPIs, any record from the field, any major or critical Alarm, or any scheduled changes in the network during the occurrence of the fault).</p>

#### Step 5. Tickets and alarms of sites from serving cells and neighboring cells.

<p>After identifying the cell and the neighbors, looking into possible sources and history of failure, extracting the logs on the specified cell and sites are valuable source of information for trouble shooting. The current major or critical alarms plus a brief history of major and critical alarm view is important input for problem solving; In addition defining the relationship between the Alarms and the ticket will gives important insight into finding the cause of the failure.</p>
Hawk will extract the Tickets and related logs from the ticketing system of the service provider for the time of the failure plus a brief history of the issues with the main cell sites and its neighbor cells. Hawk will point out the correlation between the Alarms and the Ticketing system. (Which Alarms correspond to what ticket).</p>

#### Step 6. Checking the physical parameters. (e.g.  Electrical tilt).

<p>When issues like lack of coverage or interference are the potential cause of the issue, checking the physical parameters may shed light on analyzing the issue. Currently the most popular physical parameter that can be checked is the electrical tilt (this option may not be available on all cells). However when the option of remote tilt check is not available a field team of engineers must go to the cell site and report the status of the tilt. Checking the status of the orientation of the cell (Antenna), the height of the antenna and potential blockage in front of that antenna are very important factors that should be within desired settings. An initial audit of the status of such physical parameters are critical to solving the problem.</p>
<p>Hawk will make an initial audit on the physical parameters of the cell to which the user was linked during the appearance of the fault. Also the neighboring cells and any other potential interfering cell in the area of the fault would highlight any abnormalities. </p>

#### Step 7. KPI: The major KPIs should be checked including availability, retain ability, mobility, congestion. (Transmission and Radio Nodes and Core).

<p>Main KPIs from Radio access network and some selected KPIs from the transmission and core of the network needs to be checked for any abnormality and signs of trouble. KPIs are related to the serving cells and neighboring cells, at the same time the KPIs on higher nodes such as BSC and RNC in 2G and 3G. The KPIs on the Hub sites on transmission should be checked for any sign of potential problems. Some KPIs are vendor based and need to checked trough vendor’s interfaces. </p>
<p>Hawk will look into all relevant major KPIs and highlight any abnormality of signs of potential problems with them.</p>

#### Step 8. Parameters: Related parameter to the KPI that indicates the issue should be checked.

<p>An RF engineering responsible for the Access part of mobile network is dealing with numerous tunable parameter in all nodes of the network, some examples include; Cell based such as: BTS, Node B or eNode B, higher node bases such as RNC, BSC, MCS base parameters, also the engineer has to look at some high level parameters that would indicate the health of the Core and Transmission network, All which analyzing them can be part of the problem solving process. </p>
<p>Shift or changes at times in some KPIs are a good indications of parameters that are not set correctly, or the already set parameters needs to be changed due changes that has happened in network over time such as increased traffic or added new technology or recent reorganization of the network such as frequency planning, rehoming, LAC & RAC planning and …etc. </p>
<p>Since looking at all this parameters and KPIs and correlating them can be a very time consuming task , this work can done by Hawk in a very short time period.</p>

#### Step 9. Geolocation (Coverage) & Drive test analysis around cells identified in step 4.

<p>The coverage and the quality of the signal at the fault location can be checked by looking in most updated drive test reports , this together with narrowing the serving cell plus the neighbors at the location of the fault are essential inputs for identifying the cause of the reported fault.</p>
<p>Hawk can look at the existing drive test reports and zoom in into the location of the fault and in future trails could suggest if the existing faults on the drive test report are related to the reported fault.</p>

#### Step 10. Different kind of call trace. (Cell trace (Layer 3 message), (GPEH, PCHR), core traces.

<p>At times when initial trouble shooting methods will not give the results you are looking for making a similar call and tracing it will clear issue that could not be otherwise be seen, there different methods of traces and analyzing the trace result depending on the complexity of the trace is an essential source of data show the engineer the cause the fault. </p>
<p>Hawk can display the trace result in a format that is easy to compare with other reports and possibly suggest the result of the reported fault as more and more cases are collected.</p>

#### Step 11. Checking the consistency of the issue, by drive test, field visit.

<p>An issue can be an isolated event and hence it would not occur again (it was a one-time issue).</p>
<p>In order to check this or when the above mentioned checks would not help in identifying the cause of the fault, a field team will go to recreate the fault (from user’s perspective) and the result in format of log files is provided to the engineer. As the log files may contain many different test scenarios going through all the reports, identifying weaknesses or faults at the area of the reported issue can at times be time consuming.</p>

<p>Using Hawk to pinpoint weakness in signal levels or quality plus fault at and around the location of reported issue can help to speed up the problem solving considerably.</p>
 
#### In summary:

<p>Hawk can make multi-sheet reports that can be shown on several monitors at the same time, each report containing four or six windows depending on the amount of data that needs to be shown in each window. Hawk can bring all the above problem solving scenarios in one place and guide the engineer to pinpoint the cause of the problem that traditionally each would take about 2 to 3 hours of work.</p>

<p>As Hawk is trained and used for different cases overtime, the idea is for it to get more intelligence and can categorize similar issues and look for the specific solution of that issue based on the experience it gains.</p>

