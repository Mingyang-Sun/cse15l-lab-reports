# Lab Report 3 - Week 5

## ```grep -i```
Syntax:<br />
```grep -i «string» «files»```

This -i option of the grep command searches a file or files for the given string case-insensitively, which will match all the cases of the words and print matching lines. The grep command performs a case-sensitive search by default, so this will be very useful when you want to perform a search that ignores the cases since it will produce a very different output compared to a case-sensitive search.

### Example 1.
```
mingyangsun03@nuanyang docsearch % grep -i "Terminal" technical/911report/*                     
technical/911report/chapter-1.txt:    Atta and Omari arrived in Boston at 6:45. Seven minutes later, Atta apparently took a call from Marwan al Shehhi, a longtime colleague who was at another terminal at Logan Airport. They spoke for three minutes.
technical/911report/chapter-1.txt:    In another Logan terminal, Shehhi, joined by Fayez Banihammad, Mohand al Shehri, Ahmed al Ghamdi, and Hamza al Ghamdi, checked in for United Airlines Flight 175, also bound for Los Angeles. A couple of Shehhi's colleagues were obviously unused to travel; according to the United ticket agent, they had trouble understanding the standard security questions, and she had to go over them slowly until they gave the routine, reassuring answers.
technical/911report/chapter-1.txt:    The security checkpoints through which passengers, including Atta and his colleagues, gained access to the American 11 gate were operated by Globe Security under a contract with American Airlines. In a different terminal, the single checkpoint through which passengers for United 175 passed was controlled by United Airlines, which had contracted with Huntleigh USA to perform the screening.
technical/911report/chapter-1.txt:    All five hijackers passed through the Main Terminal's west security screening checkpoint; United Airlines, which was the responsible air carrier, had contracted out the work to Argenbright Security.
technical/911report/chapter-1.txt:    About 20 minutes later, at 7:35, another passenger for Flight 77, Hani Hanjour, placed two carry-on bags on the X-ray belt in the Main Terminal's west checkpoint, and proceeded, without alarm, through the metal detector. A short time later, Nawaf and Salem al Hazmi entered the same checkpoint. Salem al Hazmi cleared the metal detector and was permitted through; Nawaf al Hazmi set off the alarms for both the first and second metal detectors and was then hand-wanded before being passed. In addition, his over-the-shoulder carry-on bag was swiped by an explosive trace detector and then passed. The video footage indicates that he was carrying an unidentified item in his back pocket, clipped to its rim.
technical/911report/chapter-1.txt:    At 9:32, controllers at the Dulles Terminal Radar Approach Control "observed a primary radar target tracking eastbound at a high rate of speed." This was later determined to have been Flight 77.
technical/911report/chapter-1.txt:    While the Command Center was told about this "other aircraft" at 9:01, New York Center contacted New York terminal approach control and asked for help in locating United 175.
technical/911report/chapter-1.txt:    Terminal: I got somebody who keeps coasting but it looks like he's going into one of the small airports down there.
technical/911report/chapter-1.txt:    Terminal: Got him just out of 9,500-9,000 now.
technical/911report/chapter-1.txt:    Terminal: We're just, we just we don't know who he is. We're just picking him up now.
technical/911report/chapter-1.txt:    The Command Center kept looking for American 77. At 9:21, it advised the Dulles terminal control facility, and Dulles urged its controllers to look for primary targets. At 9:32, they found one. Several of the Dulles controllers "observed a primary radar target tracking eastbound at a high rate of speed" and notified Reagan National Airport. FAA personnel at both Reagan National and Dulles airports notified the Secret Service. The aircraft's identity or type was unknown.
technical/911report/chapter-12.txt:                terminals. About 6,000 agencies provide transit services through buses, subways,
technical/911report/chapter-13.2.txt:            3. The call was placed from a pay phone in Terminal C (between the screening
technical/911report/chapter-13.2.txt:            4. Flight 11 pushed back from Gate 32 in Terminal B at 7:40. See AAL response to the
technical/911report/chapter-13.2.txt:                terminal checkpoints, Sept. 11, 2001.
technical/911report/chapter-13.2.txt:            14. Metropolitan Washington Airports Authority videotape, Dulles main terminal
technical/911report/chapter-13.2.txt:            15. Metropolitan Washington Airports Authority videotape, Dulles main terminal
technical/911report/chapter-13.2.txt:                general information on approaching terminals, see FAA report,"Aeronautical
technical/911report/chapter-13.2.txt:            130." N90 [New York Terminal Radar Approach] controller stated 'at approximately 9:00
technical/911report/chapter-13.3.txt:                screener. The terminal was evacuated, and police found miscellaneous gun parts,
technical/911report/chapter-13.5.txt:                interview 4, Port Authority Bus Terminal Command (Nov. 20, 2003). For officers
technical/911report/chapter-13.5.txt:                interview 4, Port Authority Bus Terminal Command (Nov. 20, 2003); NYPD interview 10,
technical/911report/chapter-13.5.txt:                interview 4, Housing (Feb. 17, 2004); PAPD interview 4, Port Authority Bus Terminal
technical/911report/chapter-13.5.txt:                desk's instructions, see PAPD statement 10, Port Authority Bus Terminal Command,
technical/911report/chapter-13.5.txt:                statement 6, Port Authority Bus Terminal Command, Jan. 4, 2002. For poor situational
technical/911report/chapter-13.5.txt:                ground floors, see PAPD interview 4, Port Authority BusTerminal Command (Nov. 20,
technical/911report/chapter-13.5.txt:                Terminal Command (Nov. 6, 2004); NYPD interview 10, ESU (Mar. 1, 2004); FDNY
technical/911report/chapter-13.5.txt:                interview 4, Port Authority Bus Terminal Command (Nov. 20, 2003).
```
This ```grep -i "Terminal" technical/911report/*``` command performs a case-insensitive search on string "Terminal" in all files within the technical/911report path. Without the use of the -i option, the result of this grep command will not include those files that have the lowercase terminal word.

### Example 2.
```
mingyangsun03@nuanyang docsearch % grep "Scientific" technical/plos/journal.pbio.0020156.txt
        Scientific societies serve their members, their broader scholarly communities, and the
        Scientific societies perform an array of tremendously valuable functions for their
mingyangsun03@nuanyang docsearch % grep -i "Scientific" technical/plos/journal.pbio.0020156.txt
        Scientific societies serve their members, their broader scholarly communities, and the
        access to scientific publications is good for scientists and good for science. Society
        are committed to catalyzing innovations within and across scientific disciplines—and
        information globally in order to accelerate the rate of scientific progress. Many societies
        implications for scientific societies. As any systemic change in research or publishing
        the scholarly associations that often serve as the backbones of scientific communities.
        Scientific societies perform an array of tremendously valuable functions for their
        Reaching a “steady-state” system of open-access publishing by scientific societies will
        become more established, however, and as the benefits of open access to scientific and
        for any scientific society to take—and PLoS welcomes the questions, comments, and feedback
```
This ```grep -i "Scientific" technical/plos/journal.pbio.0020156.txt``` command performs a case-insensitive search on string "Scientific" in the file journal.pbio.0020156.txt within the path technical/plos. Without the use of the -i option, the result of this grep command will not include those files that have the lowercase scientific word.

### Example 3.
```
mingyangsun03@nuanyang docsearch % grep "LEGAL" technical/government/About_LSC/Comments_on_semiannual.txt
LEGAL SERVICES CORPORATION BOARD OF DIRECTORS
mingyangsun03@nuanyang docsearch % grep -i "LEGAL" technical/government/About_LSC/Comments_on_semiannual.txt
LEGAL SERVICES CORPORATION BOARD OF DIRECTORS
I am pleased to transmit the comments of the Legal Services
our goal of providing high quality legal assistance to the poor of
Douglas S. Eakeley, Chairman Legal Services Corporation May 31,
State Planning Report from the Legal Services Corporation, issued
of legal services delivered by programs,2 and forged new and deeper
Since 1998, LSC has restructured legal services programs in 24
?? function as a concerted, coherent, closely coordinated legal
?? develop additional resources to expand legal services;
quality legal services;
?? target legal services resources to achieve the greatest
state communities of justice - integrated and coordinated legal
continues to assist recipients in improving the quality of legal
Legal Services Corporation
The Legal Services Corporation is a private, non-profit
corporation established in the District of Columbia by the Legal
provide financial support for legal assistance in civil proceedings
to persons unable to afford legal services. LSC is governed by an
legal services to indigent persons across the country. Of the funds
the effectiveness of the delivery of legal assistance by its
initiative for statewide planning and coordination of legal
maintenance of high quality legal assistance to eligible
legal services programs throughout the nation by improving access
to legal services while enhancing their quality. The Plan
expanding access to, and availability of, civil legal services
legal services delivery system.
resources for civil legal services, new and more efficient ways of
providing legal information and advice to low-income persons, and
the potential for half of the states to provide clients with legal
to Justice Conference; the EJC; the National Legal Aid and Defender
conference of representatives from legal services, state courts,
To assure the provision of high quality legal assistance to
programs provide referrals and community legal education, engage in
?? Referrals; ?? Community legal education presentations; ??
Community legal education materials, articles and web sites; ?? Pro
clients to obtain critical legal services from LSC recipients. The
the legal services community can better empower, strengthen and
enhance the lives of legal services clients. It convened client and
community advocates, as well as legal services staff who embrace
the concept of client-centered legal services.
Sixteen (16) conference papers were written by legal services
advocates facilitate client-centered legal services delivery in
National Legal Aid and Defender Association and the Management
Legal Affairs and the Office of Information Management, with the
legal services. As part of this project, LSC solicited public
```
This ```grep -i "LEGAL" technical/plos/journal.pbio.0020156.txt``` command performs a case-insensitive search on string "LEGAL" in the file Comments_on_semiannual.txt within the path technical/government/About_LSC. Without the use of the -i option, the result of this grep command will only include those files that have the exact uppercase LEGAL word.

## ```grep -l```
Syntax:<br />
```grep -l «string» «files»```

This -l option of the grep command searches a file or files for the given string, but only prints the names of files that contain the matched string instead of printing all the matching lines. This -l option of the grep command is very useful when you just trying to look for the files containing the string words that you are searching for because only the names of files containing selected lines are written to standard output by using this command option.

### Example 1.
```
mingyangsun03@nuanyang docsearch % grep -l "base pair" technical/biomed/*
technical/biomed/1471-2091-3-4.txt
technical/biomed/1471-2105-2-8.txt
technical/biomed/1471-2105-2-9.txt
technical/biomed/1471-2105-3-18.txt
technical/biomed/1471-2105-3-2.txt
technical/biomed/1471-2105-3-24.txt
technical/biomed/1471-2105-4-27.txt
technical/biomed/1471-2121-1-2.txt
technical/biomed/1471-2121-3-10.txt
technical/biomed/1471-213X-1-4.txt
technical/biomed/1471-2156-2-17.txt
technical/biomed/1471-2156-2-3.txt
technical/biomed/1471-2156-2-7.txt
technical/biomed/1471-2156-3-16.txt
technical/biomed/1471-2156-3-4.txt
technical/biomed/1471-2164-2-1.txt
technical/biomed/1471-2164-2-4.txt
technical/biomed/1471-2164-2-7.txt
technical/biomed/1471-2164-3-13.txt
technical/biomed/1471-2164-3-31.txt
technical/biomed/1471-2164-3-35.txt
technical/biomed/1471-2164-3-6.txt
technical/biomed/1471-2164-3-7.txt
technical/biomed/1471-2164-4-14.txt
technical/biomed/1471-2164-4-16.txt
technical/biomed/1471-2164-4-2.txt
technical/biomed/1471-2164-4-21.txt
technical/biomed/1471-2164-4-25.txt
technical/biomed/1471-2180-1-12.txt
technical/biomed/1471-2180-1-31.txt
technical/biomed/1471-2180-1-34.txt
technical/biomed/1471-2180-2-13.txt
technical/biomed/1471-2180-2-38.txt
technical/biomed/1471-2180-3-13.txt
technical/biomed/1471-2180-3-15.txt
technical/biomed/1471-2199-2-12.txt
technical/biomed/1471-2199-2-5.txt
technical/biomed/1471-2199-3-17.txt
technical/biomed/1471-2202-2-12.txt
technical/biomed/1471-2202-3-16.txt
technical/biomed/1471-2202-3-7.txt
technical/biomed/1471-2210-2-14.txt
technical/biomed/1471-2229-2-3.txt
technical/biomed/1471-2334-3-12.txt
technical/biomed/1471-2350-2-2.txt
technical/biomed/1471-2350-2-8.txt
technical/biomed/1471-2377-3-4.txt
technical/biomed/1471-2458-3-5.txt
technical/biomed/1471-2474-2-1.txt
technical/biomed/1472-6750-1-13.txt
technical/biomed/1475-4924-1-5.txt
technical/biomed/1477-7827-1-23.txt
technical/biomed/ar297.txt
technical/biomed/ar409.txt
technical/biomed/ar774.txt
technical/biomed/bcr570.txt
technical/biomed/bcr571.txt
technical/biomed/bcr602.txt
technical/biomed/bcr631.txt
technical/biomed/gb-2000-1-1-research002.txt
technical/biomed/gb-2001-2-12-research0054.txt
technical/biomed/gb-2001-2-3-research0008.txt
technical/biomed/gb-2001-2-4-research0010.txt
technical/biomed/gb-2001-2-4-research0011.txt
technical/biomed/gb-2001-2-4-research0014.txt
technical/biomed/gb-2001-2-6-research0021.txt
technical/biomed/gb-2001-2-7-research0025.txt
technical/biomed/gb-2001-2-8-research0027.txt
technical/biomed/gb-2002-3-10-research0053.txt
technical/biomed/gb-2002-3-12-research0079.txt
technical/biomed/gb-2002-3-12-research0083.txt
technical/biomed/gb-2002-3-6-research0029.txt
technical/biomed/gb-2003-4-4-r24.txt
technical/biomed/rr196.txt
```
This ```grep -l "base pair" technical/biomed/*``` command displays the name of the files in technical/biomed that contain the string "base pair". Without the use of the -l option, the output of this grep command will be all the lines in those files that contain the string base pair.

### Example 2.
```
mingyangsun03@nuanyang docsearch % grep -l "Report" technical/911report/*
technical/911report/chapter-1.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-3.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
```
This ```grep -l "Report" technical/911report/*``` command displays the name of the files in technical/911report that contain the string "Report".  Without the use of the -l option, the output of this grep command will be all the lines in those files that contain the string report.

### Example 3.
```
mingyangsun03@nuanyang docsearch % grep -l -i "Report" technical/911report/* 
technical/911report/chapter-1.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
technical/911report/chapter-12.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-2.txt
technical/911report/chapter-3.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-8.txt
technical/911report/chapter-9.txt
technical/911report/preface.txt
```
This ```grep -l -i "Report" technical/911report/*``` command displays the name of the files in technical/911report that contain the string "Report" case-insensitively because using the -i option allows the grep command to perform a case-insensitive search. Command line options can be used together, with the use of these two commands, the output is just the file names that contain the string Report ignoring cases.

## ```grep -r```
Syntax:<br />
```grep -r «string» «directory»```

This -r option of the grep command searches all files recursively for the given string, which allows searching in all the files under the current directory and its subdirectories. The grep command only allows searching for the given string in one or multiple files by default, so this command is very useful when you want to search all the files within a directory and its subdirectories.

### Example 1.
```
mingyangsun03@nuanyang docsearch % grep -r "lab report" technical
technical/plos/journal.pbio.0020145.txt:        to do literature searches for their lab reports, papers, seminars, and of course original
technical/biomed/1477-7827-1-54.txt:        Our lab reported a significant increase of Spam1 in
technical/biomed/1471-2156-2-17.txt:          pathology lab report, disease progression and
```
This ```grep -r "lab report" technical``` command searches for the given string "lab report" recursively in all files within the directory technical. Without the use of the -r option, the grep command will not execute because technical is a directory.

### Example 2.
```
mingyangsun03@nuanyang docsearch % grep -r -l "Report" technical/biomed 
technical/biomed/1471-2369-3-9.txt
technical/biomed/1471-2334-3-9.txt
technical/biomed/1468-6708-3-10.txt
technical/biomed/gb-2001-2-7-research0025.txt
technical/biomed/1472-6963-2-10.txt
technical/biomed/1471-2156-2-1.txt
technical/biomed/gb-2002-3-9-research0046.txt
technical/biomed/1471-2121-3-15.txt
technical/biomed/1475-9276-1-3.txt
technical/biomed/1472-6904-2-5.txt
technical/biomed/ar795.txt
technical/biomed/cc1843.txt
technical/biomed/1471-2458-2-16.txt
technical/biomed/cc1498.txt
technical/biomed/1471-2407-2-12.txt
technical/biomed/1472-6920-2-3.txt
technical/biomed/1471-2458-2-3.txt
technical/biomed/1471-2431-3-5.txt
technical/biomed/1471-2466-2-4.txt
technical/biomed/gb-2001-3-1-research0005.txt
technical/biomed/1471-2105-3-24.txt
technical/biomed/1471-2202-3-1.txt
technical/biomed/1471-2407-2-22.txt
technical/biomed/gb-2001-3-1-research0001.txt
technical/biomed/1471-2288-2-10.txt
technical/biomed/1471-230X-1-8.txt
technical/biomed/1471-2288-3-9.txt
technical/biomed/bcr571.txt
technical/biomed/1472-6947-1-6.txt
technical/biomed/1475-2867-2-15.txt
technical/biomed/1471-2296-3-3.txt
technical/biomed/1472-6947-1-5.txt
technical/biomed/1476-069X-2-9.txt
```
This ```grep -r -l "Report" technical/biomed``` command searches for the given string "Report" recursively in all files within the path technical/biomed, and prints out the name of the files that contain "Report" due to the use of -l option. Without the use of the -r option, the grep command will not execute because technical/biomed is a directory.

### Example 3.
```
mingyangsun03@nuanyang docsearch % grep -r -l -i "ENVIRONMENT" technical/government 
technical/government/About_LSC/Progress_report.txt
technical/government/About_LSC/Strategic_report.txt
technical/government/About_LSC/diversity_priorities.txt
technical/government/About_LSC/State_Planning_Report.txt
technical/government/About_LSC/conference_highlights.txt
technical/government/Env_Prot_Agen/multi102902.txt
technical/government/Env_Prot_Agen/section-by-section_summary.txt
technical/government/Env_Prot_Agen/jeffordslieberm.txt
technical/government/Env_Prot_Agen/final.txt
technical/government/Env_Prot_Agen/ctf1-6.txt
technical/government/Env_Prot_Agen/ro_clear_skies_book.txt
technical/government/Env_Prot_Agen/ctm4-10.txt
technical/government/Env_Prot_Agen/1-3_meth_901.txt
technical/government/Env_Prot_Agen/atx1-6.txt
technical/government/Env_Prot_Agen/tech_sectiong.txt
technical/government/Env_Prot_Agen/bill.txt
technical/government/Env_Prot_Agen/nov1.txt
technical/government/Env_Prot_Agen/tech_adden.txt
technical/government/Alcohol_Problems/Session2-PDF.txt
technical/government/Alcohol_Problems/Session3-PDF.txt
technical/government/Alcohol_Problems/DraftRecom-PDF.txt
technical/government/Alcohol_Problems/Session4-PDF.txt
technical/government/Gen_Account_Office/d0269g.txt
technical/government/Gen_Account_Office/Testimony_cg00010t.txt
technical/government/Gen_Account_Office/GovernmentAuditingStandards_yb2002ed.txt
technical/government/Gen_Account_Office/Sept27-2002_d02966.txt
technical/government/Gen_Account_Office/d01376g.txt
technical/government/Gen_Account_Office/Statements_Feb28-1997_volume.txt
technical/government/Gen_Account_Office/pe1019.txt
technical/government/Gen_Account_Office/gg96118.txt
technical/government/Gen_Account_Office/July11-2001_gg00172r.txt
technical/government/Gen_Account_Office/d01121g.txt
technical/government/Gen_Account_Office/og96011.txt
technical/government/Gen_Account_Office/d03419sp.txt
technical/government/Gen_Account_Office/Letter_Walkeraug17let.txt
technical/government/Gen_Account_Office/og97045.txt
technical/government/Gen_Account_Office/Testimony_d01609t.txt
technical/government/Gen_Account_Office/og97050.txt
technical/government/Gen_Account_Office/Sept14-2002_d011070.txt
technical/government/Gen_Account_Office/Oct15-1999_gg00026t.txt
technical/government/Gen_Account_Office/og97052.txt
technical/government/Gen_Account_Office/og97043.txt
technical/government/Gen_Account_Office/June30-2000_gg00135r.txt
technical/government/Gen_Account_Office/d01591sp.txt
technical/government/Gen_Account_Office/Oct15-2001_d0224.txt
technical/government/Gen_Account_Office/og97041.txt
technical/government/Gen_Account_Office/InternalControl_ai00021p.txt
technical/government/Gen_Account_Office/d01186g.txt
technical/government/Gen_Account_Office/og96033.txt
technical/government/Gen_Account_Office/og96027.txt
technical/government/Gen_Account_Office/og96026.txt
technical/government/Gen_Account_Office/im814.txt
technical/government/Gen_Account_Office/og96022.txt
technical/government/Gen_Account_Office/og96023.txt
technical/government/Gen_Account_Office/og96009.txt
technical/government/Gen_Account_Office/ai00134.txt
technical/government/Gen_Account_Office/Testimony_Jul17-2002_d02957t.txt
technical/government/Gen_Account_Office/ai9868.txt
technical/government/Gen_Account_Office/Paper_Walker11-2002_acpro122.txt
technical/government/Gen_Account_Office/May1998_ai98068.txt
technical/government/Gen_Account_Office/og96045.txt
technical/government/Gen_Account_Office/d02701.txt
technical/government/Gen_Account_Office/ai2132.txt
technical/government/Gen_Account_Office/Letter_WalkerJan30-2001.txt
technical/government/Gen_Account_Office/og98045.txt
technical/government/Gen_Account_Office/og96042.txt
technical/government/Gen_Account_Office/og98046.txt
technical/government/Post_Rate_Comm/Cohenetal_CreamSkimming.txt
technical/government/Post_Rate_Comm/Mitchell_RMVancouver.txt
technical/government/Post_Rate_Comm/Cohenetal_Cost_Function.txt
technical/government/Post_Rate_Comm/Cohenetal_comparison.txt
technical/government/Post_Rate_Comm/Cohenetal_Scale.txt
technical/government/Media/Legal-aid_chief.txt
technical/government/Media/Law_Award_from_College.txt
technical/government/Media/New_Online_Resources.txt
technical/government/Media/Volunteers_Step_Up.txt
technical/government/Media/Wingates_winds.txt
technical/government/Media/Assuring_Underprivileged.txt
technical/government/Media/Crains_New_York_Business.txt
technical/government/Media/residents_sue_city.txt
technical/government/Media/Farm_workers.txt
```
This ```grep -r -l -i "ENVIRONMENT" technical/government``` command searches for the given string "ENVIRONMENT" case-insensitively and recursively in all files within the path technical/government, and prints out the name of the files that contain "ENVIRONMENT". Without the use of the -r option, the grep command will not execute because technical/government is a directory.