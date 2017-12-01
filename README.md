# school-staff-demographics

Ziv Schwartz & Jill Kahane

<h1>Final Project</h1>
We used Jupyter notebooks to check out our data and conduct our analysis. All files are linked below, or can be found with our master data files in the student, staff, acs, and analysis folders.

<h3>Link to Analysis</h3>

We focused our analysis on the four questions outlined in our final project proposal. Our investigation can be found at the link below:
<ul>
<li><a href = "https://github.com/jill-k/school-staff-demographics/blob/master/analysis/School%20Staff%20Analysis.ipynb">School Staff Analysis</a></li>
</ul>

<h3>Data Checkout Details</h3>

We used data from the Massachusetts Department of Secondary and Elementary Education (DESE) website and the American Community Survey (ACS). We originally planned to use data through the 2015-2016 school year, but we found that Boston did not report staff race and ethnicity data in 2016. Since we anticipated that Boston would play a large role in our analysis, we used data from the school years 2009-2010 to 2014-2015 instead.

We used BeautifulSoup, requests, and pandas to download and process our data from the DESE website and the API to access data that we wanted from the ACS.  The master .csv file for each report can be found on GitHub in the student, staff, and acs folders, as we used only these files in our analysis. We did not commit the initial files that we downloaded.

The staff race/ethnicity master file required the most processing in the checkout stage, as we knew we wanted to conduct our analysis by job category (e.g. Teacher, School Leader, Administrative Support) instead of by the 65 distinct job codes.
<ul>
<li><a href = "https://github.com/jill-k/school-staff-demographics/blob/master/staff_data/Checkout%20-%20Staff%20Demo%20Data.ipynb"> Staff Race/Ethnicity</a></li>
</ul>

We used a similar checkout process for all of the reports listed below:
<ul>
<li><a href = "https://github.com/jill-k/school-staff-demographics/blob/master/student_data/Checkout%20-%20Student%20Race%20and%20Ethnicity%20Data.ipynb">Student Race/Ethnicity</a></li>
<li><a href = "https://github.com/jill-k/school-staff-demographics/blob/master/student_data/Checkout%20-%20School%20Addresses.ipynb">School Addresses</a></li>
<li><a href = "https://github.com/jill-k/school-staff-demographics/blob/master/student_data/Checkout%20-%20Student%20Enrollment.ipynb">Student Enrollment</a></li>
<li><a href = "https://github.com/jill-k/school-staff-demographics/blob/master/student_data/Checkout%20-%20Student%20Mobility.ipynb">Student Mobility Indicators</a></li>
<li><a href = "https://github.com/jill-k/school-staff-demographics/blob/master/student_data/Checkout%20-%20Student%20Suspension%20Data.ipynb">Student Suspension Indicators</a></li>
</ul>

We were unable to download the updated school-wide attendance report from the DESE website, so we had to download this data by looping through individual school sites and extracting the attendance indicators we needed from the HTML.
<ul>
<li><a href = "https://github.com/jill-k/school-staff-demographics/blob/master/student_data/Checkout%20-%20Student%20Attendance.ipynb">Student Attendance Indicators</a></li>
</ul>

For the ACS data, we used the API to create a master dataframe of zip-code level data for variables of interest.
<ul>
<li><a href="https://github.com/jill-k/school-staff-demographics/blob/master/acs/ACS%20Data%20Checkout.ipynb">ACS Checkout</a></li>
</ul>


<h1>Final Project Proposal</h1>

<h3>Background:</h3>

There is a growing body of research about how a diverse teaching staff benefits all students and can have particularly important impact on students of color (<a href="http://www.nber.org/papers/w8432.pdf">TS. Dee, 2001</a>; <a href="http://research.upjohn.org/cgi/viewcontent.cgi?article=1248&context=up_workingpapers">S. Gershenson, 2015</a>; <a href="http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.455.7083&rep=rep1&type=pdf">T. Pettigrew, 2006</a>). However, while the number of non-white public school students is increasing across the country, <a href="http://www.shankerinstitute.org/sites/shanker/files/The%20State%20of%20Teacher%20Diversity%20%283%29_0.pdf">the number of non-white teachers and principals is not</a>.

In the 2016-2017 school year, 90.3% of Massachusetts public school staff members reported as white while only 61.3% of students enrolled in Massachusetts public schools reported as white. We would like to use Massachusetts Department of Elementary and Secondary Education (DESE) and American Community Survey (ACS) data to investigate the following questions about school staff demographics in traditional public and charter schools. The comparison to charter schools will allow us to further our understanding of the issue.

<h3>Questions:</h3>

<ol>
<li>What is the breakdown of staff race/ethnicity within the following school employee roles in Massachusetts: principal, administrator, teacher, and support staff? (DESE)</li>
<li>Is there a correlation between the percent of non-white students and percent of non-white staff (in general and by groups mentioned above) in Massachusetts schools? (DESE)</li>
<li>Do schools with the highest percentages (top 25%) of non-white staff members have shared characteristics? What differentiates them from the schools with the lowest percentages (bottom 25%) of non-white staff members? We would like to examine the following:<ul></li>
  <li>Principal and administrator race/ethnicity (DESE)</li>
  <li>Grade levels served (DESE)</li>
  <li>Charter versus public (DESE) </li>
  <li>Race/ethnicity of residents in zip code (ACS)</li>
  <li>Race/ethnicity of public school students in zip code (DESE)</li>
  <li>Median income, percent poverty, and percent bachelor’s degrees by zip code (ACS)</li></ul>
  <li>Are there differences in key measures of student success based on staff demographics? To explore this question, we will compare groups of schools with similar student enrollment and different staff demographics and examine the below measures:<ul></li>
  <li>Attendance rates (DESE)</li>
  <li>Student mobility rates (DESE)</li>
  <li>Suspension rates (DESE)</li>
  </ul></ol>

<h3>Potential Extensions:</h3>
<ul>
<li>There are additional data points from both DESE and ACS that we could examine, such as average teacher salary by zip code, and standardized test results by school.</li>
<li>Create an visualization of the changing student and staff member demographics by year that can be filtered by zip code or school.</li>
<li>Create a dashboard for school staff members or parents that allows them to see school demographic information and success measures compared to other schools in the district.</li>
</ul>

<h3>Data:</h3>

<b>MA Department of Elementary and Secondary Education Data:</b>

We will use the following reports from the DESE website to access data from the last 5 years:
<ul>
<li><a href="http://profiles.doe.mass.edu/search/search.aspx?leftNavId=11238">
  School addresses and zip codes (to merge with ACS data)</a></li>
<li><a href="http://profiles.doe.mass.edu/state_report/teacherbyracegender.aspx">
  Staff race and ethnicity by school, overall and by position</a></li>
<li><a href="http://profiles.doe.mass.edu/state_report/enrollmentbyracegender.aspx">
  Student race and ethnicity by school</a></li>
<li><a href="http://profiles.doe.mass.edu/statereport/indicators.aspx">
  School attendance rates</a></li>
<li><a href="http://profiles.doe.mass.edu/state_report/ssdr.aspx">
  Percent of students suspended<a/></li>
<li><a href="http://profiles.doe.mass.edu/state_report/mobilityrates.aspx">
  Student mobility</a></li>
</ul>

<b>American Community Survey Data:</b>

We will use the <a href="https://www.census.gov/data/developers/data-sets/acs-5year.html">
2015 ACS 5-year estimates</a> for Massachusetts zip codes to access the following data:
<ul>
  <li>B15003: EDUCATIONAL ATTAINMENT FOR THE POPULATION 25 YEARS AND OVER</li>
  <li>S1901: INCOME IN THE PAST 12 MONTHS (IN 2015 INFLATION-ADJUSTED DOLLARS)</li>
  <li>B03002: HISPANIC OR LATINO ORIGIN BY RACE</li>
</ul>


<h3>Past Research/Articles:</h3>
<ul>
  <li>https://www.theatlantic.com/education/archive/2016/06/principals-of-color/488006/</li>
<li>https://www.theatlantic.com/education/archive/2015/09/teacher-diversity-viz/406033/</li>
<li>http://hechingerreport.org/hire-black-principals/</li>
<li>https://nces.ed.gov/pubs2016/2016189.pdf</li>
<li>http://www.newschools.org/news/education-organizations-need-to-diversify-their-leadership/</li>
<li>https://www.bostonglobe.com/metro/2017/02/12/mass-students-are-increasingly-diverse-but-their-teachers-are-not/fiwxsW4sJCdCz4wZEjLYpL/story.html</li>
<li>http://www.nber.org/papers/w8432.pdf</li>
<li>http://ftp.iza.org/dp10630.pdf</li>
</ul>
