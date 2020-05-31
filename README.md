# <img src="Hawk.png" width="134" height="75"> Hawk 
## <i>"A Mobile Network Operators Consulting"</i>

### INTRODUCTION

<P>Mobile networks have become both the generators and carriers of massive data. Big data analytics can improve the performance of mobile networks and maximize the revenue of operators. Big data technology brings about new opportunities to telecom operators faced with increasingly complex networks. Operators can use Big data technology to improve operational efficiency and network intelligence. A significant feature of Big data analytics is real-time processing. With Big data analytics, operators can monitor their infrastructure in real-time, and make autonomous plus dynamic decisions, and schedule activities. This creates new market opportunities, optimizes the network, minimizes operation and maximizes the revenue of operators. Consulting software will certainly bring great benefits such as user satisfaction, operation efficiency, and business innovation for telecom operators.</P>

<figure>
<img src="High Level Design/Hawk_NetworksDiagram.png" width="%100" height="%100">
</figure>
 
### BIG DATA FOR MOBILE OPERATORS
<P>   Big data fundamentally is not only storing and managing data – it is also deploying powerful real-time analytics and visualization tools, collaboration platforms and the ability to automatically create links with existing applications vital to the operator’s business. The first step is to collect data from a variety of sources such as network and non-network, structured and unstructured.</P>
<P>   Big data technology can address problems associated with rapid data growth, scalability, and high cost. Telecom operators might produce 10TB of raw data per day and store the same in a file format. After processing, data is reduced to 550 GB and saved in a database format. This data is often archived for a long time. Handling such a large amount of data is quite difficult for the traditional file system with a relational database.</P>
<P>   A NoSQL database can handle up to a PB of data and moreover, a stream handling and analysis platform can handle huge amounts of event data in real time, also it can handle standardization and integrity of inputs. </P>
<P>   Today, Big data is understood more or less from a technology perspective: the possibility of better storage (volume), the ability to process information and make it available in real-time (velocity) and the ability to deal with various kinds of data sources, including structured, semi-structured and unstructured ones (variety). </P>

### DATA COLLECTION 
<P> Big data in mobile networks can be obtained from either internal or external sources. Data collection methods can be divided into two categories: </P> 
<ol>
<li>Through data sources.</li>
<li>Via auxiliary tools. </li>
</ol>  
<P>The data comes from Customer Relationship Management (CRM), Operation/Business Support Systems (OSS/BSS), drive test equipment, walk test equipment, network planning, performance management, fault management, marketing & sales plan, configuration management, signaling data, transmission data and geological locations. </P>

#### A.	DATA SOURCE COLLECTION
<p>The mobile service provider needs to support data collection as shown in Figure 1, from various heterogeneous data sources in order to accurately reflect the quality of end-to-end services and customer experience. Some data sources include: </p>
<ul>
 <li><i><b>Customer Relation Management:</b></i> This includes detailed customer information such as subscription profile, IMSI, trouble ticket, and SLA.</li>
<li><i><b>Active Probing:</b></i> This includes test pack that is added to the existing network to obtain end-to-end metric data.</li>
<li><i><b>Passive Probing:</b></i> This is used when professional staff puts probes into the network interfaces, such as A/Gn interfaces, etc. to collect the signaling data.</li> 
<li><i><b>Performance Management:</b></i> This includes network access KPIs and network element KPIs, both of which are obtained through the OMC or NMS interface.</li>
<li><i><b>xDR data:</b></i> This includes MR, CDR and TDR data, which are delivered through relative interfaces on the equipment.</li>
<li><i><b>Configuration Management:</b></i> This provides detailed configuration data for network elements, including but not limited to eNodeB, MME, SGW, PGW, HSS, SGSN, MSC, and BSC/RNC.</li>
<li><i><b>Site Inventory:</b></i> This provides site information based on a date such as a site type, tower height, radio, transmission equipment, antenna type, azimuth, power system, tilts, etc.</li>
</ul>

 <figure>
 <img src="High Level Design/Hawk_DataSourceCollections.png" width="%65" height="%65">
 <figcaption>Figure 1: Data Source collection and analytics stack</figcaption>
 </figure>
 <br />

#### B.	FROM DATA TO INSIGHT 
<p>Successful decision-making will increasingly be derived from analytics-generated insights. The more accurate and timely they are, the better chance a decision-maker has to anticipate and profit from change. The key to effective data-driven decision-making is the ability to sift through large amounts of data; and the ability to combine data from several sources to gain a more comprehensive view of the problem. For example, drive test comparisons combined with performance data, fault management, and physical antenna characteristics.</p>
<p>Insights may be derived from properly correlated data. Insights can be exposed through an integrated and interactive platform that implements or reuses existing APIs and SDKs, allowing multiple applications to be supported by the same underlying data infrastructure. Overall, insights can dynamically change network performance to ensure an optimal subscriber experience.</p>

#### C.	ANALYSIS AND PREPROCESSING 
<p>The large-scale collected datasets reside at different locations with different formats. Thus, the gathered datasets are usually in a raw state with much redundancy, inconsistency or useless information. Meanwhile, the complicated vast amount of semi-structured and unstructured data make it impossible to fit them into the relational database with tables of columns & rows. NoSQL databases are becoming the alternative technology for Big data. To avoid unnecessary storage space, and ensure the processing efficiency, the data should be preprocessed to be ready for data analysis, before it is loaded into the database. These processes also involve massive distributed file systems, parallel computing frameworks, NoSQL databases, real-time streaming processing, intelligent pattern recognition, natural language understanding, and expert knowledge bases. For example, in order to correlate and normalize the dataset, the data collected from mobile Apps, geolocation, network logs, CDRs, and weblogs will not be stored directly in a storage system until it is preprocessed. Three common data preprocessing techniques are integration, cleaning and redundancy elimination.</p>

#### D.	BIG DATA ANALYTICS PLATFORMS AND TOOLS 
<p><i>“Apache Hadoop”</i> is an open-source software framework for distributed storage and distributed processing of large-scale datasets. The power of clusters enforces Hadoop to store and process data at high-speed. Initially, Hadoop was developed for routine functions as a keyword classification on search engines. To cater for the requirements of various business applications, Hadoop gradually turned into general-purpose Big data operating platforms, where different data manipulations and data analytical operations can be plugged into. All the features make Hadoop particularly adept at processing or analyzing the data in mobile networks, such as Network KPI, CRM, drive test result, marketing plan, etc. this data needs to be retrieved from storage systems for analysis frequently. Meanwhile, various suitable data analysis methods for mobile networks can be integrated into Hadoop platforms.</p>

<figure>
<img src="High Level Design/Hawk_Framework.png" width="%65" height="%65">
<figcaption>Figure 2: Hawk Framework</figcaption>
</figure>
<br />
<br />

<p><i>“Apache Spark”</i> is a popular open-source platform for large-scale data processing that is well-suited for iterative machine learning tasks. Figure 2, shows a Big data analytics framework. By allowing user programs to load data into a cluster’s memory and query it repeatedly. Spark is a unified analytics engine complete with machine learning algorithms and libraries. In contrast to Hadoop’s two-stage disk-based MapReduce paradigm, Spark’s multi-stage in-memory primitives provide performance up to 100 times faster for certain applications.</p>
<p><i>“Flume Agent”</i> is a distributed, reliable, and available service for efficiently collecting, aggregating, and moving large amounts of log data. It has a simple and flexible architecture based on streaming data flows.</p>
<p>For this architecture we have designed analogous hardware, figure 3. shown block diagram architecture.</p>

<figure>
<img src="High Level Design/Hawk_BlockDiagram.png" width="%65" height="%65">
<figcaption>Figure 3: Hawk Block Diagram</figcaption>
</figure>
<br />


### USE CASE STUDIES OF BIG DATA ANALYTICS IN MOBILE OPERATORS 
<p>The following use case studies provide an illustration of introducing Big data analytics to mobile operators. The focus is on improving network performance, deriving valuable insights, and making the right decisions. In addition, the using search engines in any situation helps us obtain more information. Figure 3 shows a sample combination of network access applications, used in popular industrial applications for multi-vendors in a mobile network.</p>

#### A.	Engineering level - Customer Claim use case
<p> Some mobile customers report major network issues such as poor coverage or lack of signal of the mobile provider. They register customer claim by CRM application and create a new trouble ticket.</p> 
<p> CRM applications provides limited information, e.g. geolocation, IMSI, time/date and network problem. In traditional manner, service engineers often make a resource consuming effort to investigate the cause of the problem from other existing data on the network such as RAN KPI and drive test results. Data collected is stored in different departments by the different databases, different formats, and different applications. Therefore service engineers make requests to other departments for proper data. It is a de facto requirement that the engineers be experts in various applications so that they can identify the root cause of the problem and offer solutions. </p>
<p>But, if the service engineers have more information and data such as CDR, network planning, marketing plan, site inventory and other network data, they can create a powerful solution for both the fault error and other weak network areas.</p>
<p>In this case, the engineer uses Hawk’s search engine for specific location or fault information on the network. Hawk then correlates data sources, using algorithms and data mining, and presents a big picture of real-time network behavior, solution suggestions, and self-learning to suggest accurate solutions for other minor or major network problem. </p>

<p><i>For more detail please refer to Appendix II. </i></p>

<figure>
<img src="High Level Design/Hawk_UsedCases.png" width="%65" height="%65">
<figcaption>Figure 4: Big data combination network access </figcaption>
</figure>
<br />

#### B.	CTO level – Network overload traffic used case 
<p>The Chief Technical Officer obtains overload PS traffic notice by RAN KPI a 90-day trend report. The CTO traditionally requests RAN engineers to investigate by network performance using analysis tools and look close into clusters, sites or cells to recognize a cause of the problem. However, the CTO needs essential information to take appropriate action, and not jump to conclusions, whereby cooperation and collaboration between various departments are required. </p>
<p>Whereas chief level manager’s responsibilities are induction reactions over the reports. The search engine in Hawk can help provide them with more information. By correlating data sources, using algorithms and data mining, Hawk can depict network overloading by real-time screen monitoring at a glance. The CTO can attain an accuracy plan for the network by observing the managing service activities or/and streaming network expansion activity or core network performance, etc.</p>
<p>Moreover, for chief level managers, it is vital to pay attention to the granularity of input data (e.g. a drive test could be done every 3 months, performance data must be hourly, traces and GPEH could be event-based, CRM could be event-based). So aligning the inputs is a big challenge for mobile network operators. In this case, Hawk software tool can manage data alignment and analytics and potentially provide an alert to the CTO or team.</p>
<p><i>For more detail please refer to Appendix III. </i></p>

#### C.	CEO level – General Responsibility use case
<p>Some of the CEO responsibilities in mobile network operators are: to control the direction of the company, decide budgets for all departments, take responsibility for day-to-day decisions, identifying risks and ensuring appropriate strategies based on a cost & progress with marketing & sales plan, attending board meetings and other presentations. So, the best way for the CEO to have a real-time monitoring system for overseeing all activity in real-time, is with the aid of Hawk.</p>
<p>By correlating data sources, using algorithms and data mining, Hawk ensures accuracy and reliability within many aspects of concern for the CEO. Hawk ensures accuracy in the statement of financial position, statement of subscribers satisfaction and statement of marketing and investment position.</p>
<p><i>For more detail please refer to Appendix IV.</i></p>

## CONCLUSION 
<p><b>Hawk</b> is the missing link for the evolution in next-generation of mobile operator’s network.</p>
<p><b>Hawk</b> is a consulting software, which can be an indispensable part of making the mobile network operators smarter, making cost & progress more efficient and even improving the design of the next-generation mobile network architectures.</p> 
<p>In this white paper, the connection between Big data analytics and mobile operators has been systematically explored. The paper  provides a broad overview of Big data analytics based on datasets and applications such as performance tools, CRM tools, planning tools and marketing tools. Moreover, an architectural framework for the applications of Big data analytics in mobile operators was presented. Finally, several illustrative use cases in mobile operators were provided in order to illustrate usability of <b>Hawk</b> as a consulting software for telecommunication service providers.</p>

