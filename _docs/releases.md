---
title: Releases
---

<div class="col-md-12" markdown="1">

## Releases

We release new versions of the Peekbank database as new data becomes available. To ensure reproducibility, we maintain database versions associated with each publication by the Peekbank team. Visualizations and the <code>peekbankr</code> package will always use the most recent database version by default. The R API <code>peekbankr</code> can be directed to use any recent database version by using the <code>db_version</code> parameter.  

&nbsp;

<div class="row">
	<table style="width:60%;margin-left:auto;margin-right:auto">
		<tr>
			<td><h4 style="color:red;">2022.1 </h4><a name="2022.1"></a></td>
			<td>  &nbsp;&nbsp;&nbsp;</td>
			<td>Peekbank version for reproducing Zettersten et al. (2022), <i>under review</i>, <a href="https://psyarxiv.com/tgnzv" target="_blank">https://psyarxiv.com/tgnzv</a>.</td>
		</tr>
		<tr>
			<td><h4 style="color:red;">2021.1 </h4><a name="2021.1"></a></td>
			<td>  &nbsp;&nbsp;&nbsp;</td>
			<td><b>Initial release</b>. Peekbank version for reproducing Zettersten et al. (2021), <i>CogSci</i>, <a href="https://psyarxiv.com/ep693" target="_blank">https://psyarxiv.com/ep693</a>.</td>
		</tr>
	</table>
</div>

## Using Peekbank Locally

For intensive use cases, e.g. repeatedly transferring more than 5 GB of data, users may wish to download one or more  yearly releases of the database for installation on a local MySQL server (either on their own machine or a machine on their local network). The release databases can be downloaded <code>mysqldump</code> command:

<p><code> mysqldump -h $HOST_FROM_JSON -u $USER_FROM_JSON -p$PASSWORD_FROM_JSON --databases $DATABASES | mysql -u $LOCAL_USER -p$LOCAL_PASSWORD</code></p>

The first part of this command (<code>mysqldump</code>) outputs the content of the database as a text stream of SQL statements. The second part reads it into end-user's local MySQL server. We leave it as an exercise to the reader to replace the variables above (such as <code>$HOSTNAME</code>) with the correct values from the the JSON file that is used by the R package to coordinate and authorize MySQL access, <a href="https://peekbank.stanford.edu/peekbank.json"> peekbank.json</a>. The corresponence between variables is as follows:

<center>
<div class="row">
	<table style="width:60%">				  
	  <tr>
	    <td>$HOST_FROM_JSON</td><td>"host" field in JSON</td>
	  </tr>
	  <tr>
	    <td>$USER_FROM_JSON</td><td>"user" field in JSON</td>
	  </tr>
	  <tr>
	    <td>$PASSWORD_FROM_JSON</td><td>"password" in JSON</td>
	  </tr>
	  <tr>
	    <td>$DATABASES</td><td>{2021.1, peekbank_dev}</td>
	  </tr>
	  <tr>
	    <td>$LOCAL_USER</td><td>Local MySQL user (possibly <i>root</i>)</td>
	  </tr>
	  <tr>
	    <td>$LOCAL_PASSWORD</td><td>Local MySQL password for user </td>
	  </tr>
	</table>
</div>
</center>

Once you have a local MySQL installation, refer to the documentation for <code>peekbankr</code> regarding how to use a local database server. For most uses cases, using the API with the default remote server (hosted on Amazon on EC2) should be sufficient.


