<h2><a class="header" href="#aim" id="aim">Aim</a></h2>
<p>Max is a hard working IT professional who works at two different offices for <em><strong>six days of the week</strong></em>.</p>
<p>On <em><strong>even days</strong></em>, he works at office <strong>'A'</strong> in a day shift from <em><strong>1000 Hrs</strong></em> to <em><strong>1800 Hrs</strong></em>.</p>
<p>On <em><strong>odd days</strong></em>, he works at office <strong>'B'</strong> in a night shift from <em><strong>1800 Hrs</strong></em> to <em><strong>0000 Hrs</strong></em> or <em><strong>midnight</strong></em>.</p>
<p>Given a list of dates in a CSV file, find out for which office did he work on each date in the list and add the appropriate office name next to the date in the new CSV file.</p>
<p>Also find out how many <strong>hours</strong> does he work for office '<strong>A</strong>' and office '<strong>B</strong>' respectively.</p>
<p>A skeleton code stub is provided a starting point in solving the task.</p>
<p>The code stub provided below is to be used. It calls the functions <strong><code>readWorkSheet()</code></strong>, <strong><code>calculateOfficeHrs()</code></strong> and <strong><code>writeOfficeWorkSheet()</code></strong>. Your task is to complete these functions.</p>
<hr />
<h2><a class="header" href="#given" id="given">Given</a></h2>
<p>Two files are provided to solve this assigment.</p>
<ul>
<li>Skeleton program file: <strong><code>task1_bonus.py</code></strong>
<ul>
<li>The skeleton consists of three functions which you have to modify:
<ul>
<li><strong><code>readWorkSheet()</code></strong></li>
<li><strong><code>calculateOfficeHrs()</code></strong></li>
<li><strong><code>writeOfficeWorkSheet()</code></strong></li>
</ul>
</li>
</ul>
</li>
<li>Sample CSV file: <strong><code>task1_bonus_sample.csv</code></strong>
<ul>
<li>The CSV file has 2 columns: <strong><code>date</code></strong> and <strong><code>office_name</code></strong>.</li>
<li>The <strong><code>date</code></strong> column contains dates in the <strong><code>YYYY-MM-DD</code></strong> format and the <strong><code>office_name</code></strong> column is blank.</li>
</ul>
</li>
</ul>
<hr />
<h2><a class="header" href="#procedure" id="procedure">Procedure</a></h2>
<ul>
<li>
<p>Open the skeleton program file, <strong><code>task1_bonus.py</code></strong>.</p>
</li>
<li>
<p>You will notice pre-written comments included in skeleton program for your assistance to solve the task.</p>
</li>
<li>
<p>Three functions to modify are:</p>
<ul>
<li>
<h3><a class="header" href="#readworksheet" id="readworksheet"><strong><code>readWorkSheet()</code></strong></a></h3>
<table><thead><tr><th>Function Name</th><th align="center"><code>readWorkSheet()</code></th></tr></thead><tbody>
<tr><td><strong>Purpose</strong></td><td align="center">Reads the input CSV file of Work Sheet and creates a mapping of date and office name where he worked.<br>The office name should be <strong><code>A</code></strong> and <strong><code>B</code></strong> for even and odd days respectively but should be <strong><code>-</code></strong> for Sunday.</td></tr>
<tr><td><strong>Input Arguments</strong></td><td align="center"><strong><code>file_name</code></strong> : [ <em><strong>str</strong></em> ] <br> CSV file name of Work Sheet</td></tr>
<tr><td><strong>Output Arguments</strong></td><td align="center"><strong><code>date_office_name_mapping</code></strong> : [ <em><strong>dict</strong></em> ] <br> Mapping of the date and office name where he worked as { Key : Value } pair</td></tr>
<tr><td><strong>Example Call</strong></td><td align="center"><em><strong>date_office_name_mapping = readWorkSheet(csv_file_name)</strong></em></td></tr>
</tbody></table>
<br>
</li>
<li>
<h3><a class="header" href="#calculateofficehrs" id="calculateofficehrs"><strong><code>calculateOfficeHrs()</code></strong></a></h3>
<table><thead><tr><th>Function Name</th><th align="center"><code>calculateOfficeHrs()</code></th></tr></thead><tbody>
<tr><td><strong>Purpose</strong></td><td align="center">Calculate the number of hours worked in office A and B with the given mapping of date and office name.</td></tr>
<tr><td><strong>Input Arguments</strong></td><td align="center"><strong><code>mapping_dict</code></strong> : [ <em><strong>dict</strong></em> ] <br/> Mapping of the date and office name where he worked as { Key : Value } pair</td></tr>
<tr><td><strong>Output Arguments</strong></td><td align="center"><strong><code>(no_hrs_office_A, no_hrs_office_B)</code></strong> : [ <em><strong>tuple</strong></em> ] <br> Number of hours worked in office A and B as pair</td></tr>
<tr><td><strong>Example Call</strong></td><td align="center"><em><strong>total_hrs_office_A_B = calculateOfficeHrs(date_office_name_mapping)</strong></em></td></tr>
</tbody></table>
<br>
</li>
<li>
<h3><a class="header" href="#writeofficeworksheet" id="writeofficeworksheet"><strong><code>writeOfficeWorkSheet()</code></strong></a></h3>
<table><thead><tr><th>Function Name</th><th align="center"><code>writeOfficeWorkSheet()</code></th></tr></thead><tbody>
<tr><td><strong>Purpose</strong></td><td align="center">Writes a CSV file with date and office name where the person worked on each day.</td></tr>
<tr><td><strong>Input Arguments</strong></td><td align="center"><strong><code>mapping_dict</code></strong> : [ <em><strong>dict</strong></em> ] <br/> Mapping of the date and office name where he worked as { Key : Value } pair<br/> <strong><code>out_file_name</code></strong> : [ <em><strong>str</strong></em> ]<br/>File name of CSV file for writing the data to</td></tr>
<tr><td><strong>Output Arguments</strong></td><td align="center">None, but writes the data of office name for each date in the CSV file with given name.</td></tr>
<tr><td><strong>Example Call</strong></td><td align="center"><em><strong>writeOfficeWorkSheet(date_office_name_mapping, out_csv_file_name)</strong></em></td></tr>
</tbody></table>
<br>
</li>
</ul>
</li>
<li>
<p>Refer the <strong>Expected Output</strong> section below and debug your code to get the correct output.</p>
</li>
<hr>
<h2><a class="header" href="#expected-output" id="expected-output">Expected Output</a></h2>
<ul>
<li>
<p>The provided sample CSV file, <strong><code>task1_bonus_sample.csv</code></strong> consists data with fields <em><strong>date</strong></em>, <em><strong>office_name</strong></em> with <em><strong>office_name</strong></em> column as blank.</p>
</li>
<li>
<p>The content of this CSV file is shown below:</p>
<pre><code class="language-spreadsheet">date,office_name
2021-03-26,
2021-04-01,
2021-04-20,
2021-04-04,
2021-04-12,
2021-04-23,
2021-04-03,
2021-03-29,
2021-03-28,
2021-03-31,
2021-04-10,
2021-04-16,
2021-04-24,
2021-04-11,
2021-04-13,
</code></pre>
</li>
<li>
<p>The expected output of program <strong><code>task1_bonus.py</code></strong> i.e., to write the CSV file with given name, defined in <strong><code>main</code></strong> function, having the fields <em><strong>date</strong></em> and <em><strong>office_name</strong></em> is shown below:</p>
<pre><code class="language-python">{
	'2021-03-26': 'A', '2021-04-01': 'B', '2021-04-20': 'B', '2021-04-04': '-', '2021-04-12': 'A',
    '2021-04-23': 'A', '2021-04-03': 'B', '2021-03-29': 'A', '2021-03-28': '-', '2021-03-31': 'A',
    '2021-04-10': 'B', '2021-04-16': 'A', '2021-04-24': 'B', '2021-04-11': '-', '2021-04-13': 'B'
}
(48, 36)
</code></pre>
</li>
<li>
<p>The first five lines above are the output of <strong><code>readWorkSheet</code></strong> function i.e. variable <strong><code>date_office_name_mapping</code></strong> and,</p>
<p>the last line is the output of <strong><code>calculateOfficeHrs</code></strong> function i.e. variable <strong><code>total_hrs_office_A_B</code></strong>.</p>
</li>
<li>
<p>The program also generates a CSV file with the name <strong><code>output_task1_bonus_sample.csv</code></strong> as defined in <strong><code>main</code></strong> function that is then passed to <strong><code>writeOfficeWorkSheet</code></strong> function. The CSV file will have the contents as shown below:</p>
<pre><code class="language-spreadsheet">date,office_name
2021-03-26,A
2021-04-01,B
2021-04-20,B
2021-04-04,-
2021-04-12,A
2021-04-23,A
2021-04-03,B
2021-03-29,A
2021-03-28,-
2021-03-31,A
2021-04-10,B
2021-04-16,A
2021-04-24,B
2021-04-11,-
2021-04-13,B
</code></pre>
</li>
</ul>
