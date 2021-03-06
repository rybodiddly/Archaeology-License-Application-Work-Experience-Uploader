# Archaeology-License-Application-Work-Experience-Uploader
Python script to upload work experience for the Ontario Archaeology License Application

__Requirements:__
```
bs4 (BeautifulSoup)
pandas
requests
urllib3
```

__Usage:__
```
uploader.py <user_name> <password> <application_id> <csv_file> -<experience_type>

Example:
python uploader.py myusername mypassword 1234 WorkExperience.csv -we

Experience Types:
-we = general work experience
-s  = supervisor experience
-a  = artifact mangement experience
```

__How To:__

Create a new R License application online. To get your application number / ID, log in to your account, click `Applications` from the left hand menu so it drops down, then from the drop down select `Search for an Application`. Then select `New License` from the `Licence Application Type` drop down. Click Search. The following page will display your application id number. When using the uploader, you have the option of entering just the 4 digit ID or including the `APPL-` prefix.

Use the included csv file. Make sure there are no spaces after pif / borden #'s. Also make sure all stages, cultural periods and terrain types correctly match ministry requirements. Once the work experience csv is complete, use the commands detailed above to upload your work experience.

__Experience Types:__

A new Applied Research (R) License application contains 3 areas of required experience:
```
1. General Work Experience (150 day requirement)
2. Supervisory Experience
3. Artifact Management Experience
```
Because much of this data overlaps, you are able to input all the data into the supplied csv template. You can then upload your data to each section using one of the 3 experience type commands.

__Program Flow:__

`-we` uploads all rows of experience (including rows with Supervisor and Artifact Management Experience) in the csv into the Practical Work Experience section while omiting Supervisor and Artifact Management Columns.

`-s ` only uploads rows containing of Supervisor Experience to the Supervisor Experience section

`-a ` only uploads rows containing of Artifact Management Experience to the Artifact Management Experience section


# CSV Options:

__Stage Options:__
```
1
2
1&2
3
4

NOTE: Stage 4 will default to 4 EX (excavation) on application. If you wish 
to switch to A&P (avoidance and protection), you must manually edit online. 
Support for additional stage 4 options will be added int the future, but A&P 
mitigation will unlikely be utilized in R license applications.
```

__Cultural Period Options:__
```
Archaic
Euro-Canadian
Multi-component
Paleo-Indian
Post-Contact Indigenous
Woodland
Pre-Contact
Post-Contact
Industrial
Fur Trade
No Sites
Other
```
__Terrain Options:__
```
Agricultural
Arctic
Canadian Shield
Cemetery/Burial
Industrial
Marine
Open field
Park
Urban
Wooded
No Sites
Other
```

__Supervisor Experience Options:__
```
Supervisor
Co-Supervisor
Assistant Supervisor
Crew Chief
Team Lead
```

__Artifact Management Experience Options:__
```
- Identification and cataloguing of artifacts
- Statistical and interpretive analysis of artifacts
- Specialist analysis such as faunal or botanical
- Stratigraphic, feature or distribution analysis and interpretation
- Responsibility for field lab, artifact processing and packing
- Collections conservation, rehabilitation, rehousing
- Collections and/or lab policy and procedural development

Note: The above Artifiact Management Experience options were taken from the online application Instructions. 
The downloadable pdf detailing the application instructions suggested a more robust / nuanced level of detail
regarding your activities. Use the above list as a baseline, but it is in your best interest to extrapolate
on your activites / methodologies to strengthen your application.
```

__Notes:__
- currently this script is intented for new R license applications. It has not been tested with any other license or license renewal types.
- Support for additional license types will be added in the future.
