# COMMAND LINE INTERFACE (CLI) INTRODUCTION
## 1. Terminology
Node: A VM in the cluster
NodeGroup: A group of VMs with same functionality and spec
Cluster: A group of NodeGroups working together
Distro: A Hadoop distribution version

## 2. Usage
CLI supports shell mode, command line mode, and execution of script file. After compile, you can find the jar file under cli/target directory.
- Shell mode: java -jar serengeti-cli-0.1.jar. It supports tab key based command hint and completion. It supports history by up/down arrows.
- Command line mode: java -jar serengeti-cli-0.1.jar "command1;command2..."
- Execution of script file: in shell mode or command line mode, execute "script --file scriptFileName". The shell history file named cli.log will help to generate the script file. 

## 3. Command Syntax
CLI commands are built on spring shell(https://github.com/SpringSource/spring-shell), so its syntax follows spring shell command syntax below:
Command ::= serengeti <command-category> <command-name> <required-command-key-values>* [<optional-command-key-values>]*
required-command-key-values ::= <command-key-value-fullsize>
optional-command-key-values ::= <command-key-value-fullsize>
required-command-key-values-fullsize ::= <command-key-value-fullsize>
optional-command-key-value-fullsize ::= <command-key-value-fullsize>
command-key-value-fullsize ::= '--'<command-key-full> [<value>]
- Command-category is the type of object that the command will operate on.
- Command-name is the operation to do.
- Required-command-key-values are parameters that required for the operation.
- Optional-command-key-values are parameters that are optional for the operation.

## 4. Command Help
- Shell level Help: user can get shell level help by using "help" in command line mode or help command in shell mode. A list of objects will be displayed with operations and short descriptions.
- Command category level help: to get help for a particular class of object, user can enter help followed by an object. CLI will display all operations defined for the object.
- Command level help: to get help for a particular operation, user can enter help followed by an object and an operation. This will display all parameters.

## 5. Command List
<table class=MsoTableGrid border=1 cellspacing=0 cellpadding=0 width=624
 style='width:6.5in;border-collapse:collapse;border:none'>
 <tr>
  <td width=67 valign=top style='width:.7in;border:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>command-category</span></p>
  </td>
  <td width=66 valign=top style='width:49.5pt;border:solid windowtext 1.0pt;
  border-left:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>command-name</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border:solid windowtext 1.0pt;
  border-left:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Parameters</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border:solid windowtext 1.0pt;
  border-left:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>descriptions</span></p>
  </td>
 </tr>
 <tr>
  <td width=67 valign=top style='width:.7in;border:solid windowtext 1.0pt;
  border-top:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>connect</span></p>
  </td>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>&nbsp;</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--host
  &lt;Serengeti server host&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Connect
  a Serengeti server.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Remark</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>The
  Serengeti host with optional port number, e.g. hostname:port .</span></p>
  </td>
 </tr>
 <tr>
  <td width=67 rowspan=3 valign=top style='width:.7in;border:solid windowtext 1.0pt;
  border-top:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>resource
  pool</span></p>
  </td>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>add</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;resource pool name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--vcrp
  &lt; VC rp name &gt; </span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--vccluster
  &lt; vsphere cluster name &gt; </span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><a name="OLE_LINK2"></a><a name="OLE_LINK1"><span style='font-size:
  9.0pt;font-family:"Times New Roman","serif"'>None</span></a></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Add
  a new resource pool.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Remark</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>User
  must add a resource pool before create a cluster.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>&nbsp;</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>list</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;resource pool name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--detail&lt;<a
  name="OLE_LINK10"></a><a name="OLE_LINK9">flag to show </a>node
  information&gt;</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><a name="OLE_LINK4"></a><a name="OLE_LINK3"><b><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></a></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><a name="OLE_LINK12"></a><a name="OLE_LINK11"><span style='font-size:
  9.0pt;font-family:"Times New Roman","serif"'>Show resource pool information.</span></a></p>
  </td>
 </tr>
 <tr>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>delete</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;resource pool name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><a name="OLE_LINK6"></a><a name="OLE_LINK5"><b><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></a></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Delete
  an unused resource pool.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Remark</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>User
  cannot delete a resource pool which is in use.</span></p>
  </td>
 </tr>
 <tr>
  <td width=67 rowspan=3 valign=top style='width:.7in;border:solid windowtext 1.0pt;
  border-top:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>datastore</span></p>
  </td>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>add</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  <a name="OLE_LINK8"></a><a name="OLE_LINK7">&lt;data store name&gt;</a></span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--spec
  &lt;</span><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>datastore
  name(s) in the vsphere&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--type
  &lt;specify the type for storage: SHARED or LOCAL&gt;</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Add
  new datastore(s) .</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Remark</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>When
  the spec parameter include some <a name="OLE_LINK28"></a><a name="OLE_LINK27">datastore
  </a>names, users need to use &quot;,&quot; to separate them. Users may also specify
  multiple data stores by a wildcard.</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>list</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;data store name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--detail
  &lt; flag to show datastore detail information &gt;</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><a name="OLE_LINK14"></a><a name="OLE_LINK13"><b><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></a></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Show
  datastore information.</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>delete</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;data store name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Delete
  an unused datastore .</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>&nbsp;</span></p>
  </td>
 </tr>
 <tr>
  <td width=67 rowspan=3 valign=top style='width:.7in;border:solid windowtext 1.0pt;
  border-top:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>network</span></p>
  </td>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>add</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;network name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--portGroup&lt;vsphere
  port group name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><i><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Combination
  1</span></i></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--</span><span
  style='font-size:10.0pt;font-family:"Times New Roman","serif"'> </span><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>dhcp &lt; </span><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>mark as<span
  style='color:#313131'> </span>dhcp type</span><span style='font-size:9.0pt;
  font-family:"Times New Roman","serif"'>&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><i><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Combination
  2</span></i></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--</span><span
  style='font-size:10.0pt;font-family:"Times New Roman","serif"'> </span><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>ip &lt;ip range
  information&gt; </span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--</span><span
  style='font-size:10.0pt;font-family:"Times New Roman","serif"'> </span><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>dns&lt;</span><span
  style='font-size:10.0pt;font-family:"Times New Roman","serif"'> </span><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>first dns
  information &gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--</span><span
  style='font-size:10.0pt;font-family:"Times New Roman","serif"'> </span><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>secondDNS &lt;second
  dns information&gt; </span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--</span><span
  style='font-size:10.0pt;font-family:"Times New Roman","serif"'> </span><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>gateway
  &lt;gateway information&gt; </span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--</span><span
  style='font-size:10.0pt;font-family:"Times New Roman","serif"'> </span><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>mask&lt;mask
  information&gt; </span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><a name="OLE_LINK20"></a><a name="OLE_LINK19"><b><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></a></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Add
  a <a name="OLE_LINK22"></a><a name="OLE_LINK21">network </a>to Serengeti.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Remark</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Users
  must enter either ip range or dhcp, but not both.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Example</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>network
  add --name ipNetwork --ip 192.168.1.1-100,192.168.1.256-300 --portGroup pg1
  --dns 202.112.0.1 --gateway 192.168.1.255 --mask 255.255.255.1</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>network
  add --name dhcpNetwork --dhcp</span></p>
  </td>
 </tr>
 <tr style='height:31.05pt'>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:31.05pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>list</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:31.05pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;network name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--detail
  &lt;flag to show network detail information &gt;</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:31.05pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><a name="OLE_LINK24"></a><a name="OLE_LINK23"><b><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></a></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><a name="OLE_LINK36"></a><a name="OLE_LINK35"><span style='font-size:
  9.0pt;font-family:"Times New Roman","serif"'>Show network information.</span></a></p>
  </td>
 </tr>
 <tr>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>delete</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;network name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Delete
  an unused network.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Remark</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>User
  cannot delete a network which is in use.</span></p>
  </td>
 </tr>
 <tr>
  <td width=67 rowspan=6 valign=top style='width:.7in;border:solid windowtext 1.0pt;
  border-top:none;padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>cluster</span></p>
  </td>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>create</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;cluster name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--distro
  &lt; hadoop distro name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--specFile
  &lt;spec file pathname&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--rpNames
  &lt;</span><span style='font-size:10.0pt;font-family:"Times New Roman","serif"'>
  </span><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>resource
  pools for the cluster &gt; </span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--dsNames
  &lt;</span><span style='font-size:10.0pt;font-family:"Times New Roman","serif"'>
  </span><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>datastores
  for the cluster&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--networkName
  &lt;network name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--resume
  &lt;</span><span style='font-size:10.0pt;font-family:"Times New Roman","serif"'>
  </span><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>flag
  to resume cluster creation &gt;</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Create
  a Hadoop cluster</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Remark</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>The
  specFile is defined in jason format.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Example</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>cluster
  create --name testCluster</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>delete</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;cluster name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Delete
  an unused cluster.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>&nbsp;</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>resize</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;cluster name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--nodeGroup
  &lt;</span><span style='font-size:10.0pt;font-family:"Times New Roman","serif"'>
  </span><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>node
  group name&gt; </span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--instanceNum
  &lt;<a name="OLE_LINK32"></a><a name="OLE_LINK31">instance</a> number&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Change
  the number of nodes in a node group.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Parameter
  Definition</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>instance
  number ::= &lt;final number&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Remark</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>The
  instanceNum should be larger than the existing instance numbers in the node
  group.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Example</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>cluster
  resize --name testCluster --nodeGroup slave -- instanceNum 10</span></p>
  </td>
 </tr>
 <tr style='height:47.2pt'>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:47.2pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>start</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:47.2pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;cluster name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:47.2pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Start
  VMs in a cluster.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>&nbsp;</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>stop</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;cluster name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Stop
  VMs in a cluster.</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>&nbsp;</span></p>
  </td>
 </tr>
 <tr>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>list</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  <a name="OLE_LINK34"></a><a name="OLE_LINK33">&lt;cluster name&gt;</a></span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--detail
  &lt;flag to show node information&gt;</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><a name="OLE_LINK38"></a><a name="OLE_LINK37"><b><span
  style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></a></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Show
  cluster information.</span></p>
  </td>
 </tr>
 <tr style='height:31.0pt'>
  <td width=67 valign=top style='width:.7in;border:solid windowtext 1.0pt;
  border-top:none;padding:0in 5.4pt 0in 5.4pt;height:31.0pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>distro</span></p>
  </td>
  <td width=66 valign=top style='width:49.5pt;border-top:none;border-left:none;
  border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:31.0pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>list</span></p>
  </td>
  <td width=216 valign=top style='width:2.25in;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:31.0pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Mandatory</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>None</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Options</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--name
  &lt;distro name&gt;</span></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>--detail
  &lt;</span><span style='font-size:10.0pt;font-family:"Times New Roman","serif"'>
  </span><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>flag
  to show <a name="OLE_LINK40"></a><a name="OLE_LINK39">distro </a>detail
  information&gt;</span></p>
  </td>
  <td width=275 valign=top style='width:206.1pt;border-top:none;border-left:
  none;border-bottom:solid windowtext 1.0pt;border-right:solid windowtext 1.0pt;
  padding:0in 5.4pt 0in 5.4pt;height:31.0pt'>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><b><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Function</span></b></p>
  <p class=MsoNormal style='margin-bottom:0in;margin-bottom:.0001pt;line-height:
  normal'><span style='font-size:9.0pt;font-family:"Times New Roman","serif"'>Show
  distro information.</span></p>
  </td>
 </tr>
</table>
