# C$WP
============

C$WP   stands    for  a    Loosely coupled  Type-0 remoteweb/web application.    it  is   invented  by  wilmix  jemin j .


SYNTAX
======



<?language=C$> //indicates   that  remote  /webapplication     using  cjava



<IMPORT>  java.util.*; //load  cjava util packages.
 

<%




public class <Classname> {


  public void main() // main function  of  Cjava
{


//loosely  coupling  using  Cjava

@ <looselycoupledvariable>#;

<looselycoupledvariable>!(100000);

int yo=Integer.<PARSE>Int(<looselycoupledvariable>$.StringConvert()) + 5;
  
 //at  first  convert  to  string  and  then  convert  to integer....





 
}

}



%>


?>


index.cdollar
===========

<?language=C$>



<IMPORT>  java.util.*;
 

<%




public class index {


  public void main()
{

HTML.displayhtml("BILL.html");

//loosely  coupling  using  Cjava

@ y#;

y!(100000);

int yo=Integer.<PARSE>Int(y$.StringConvert()) + 5;

CDollar.Println(""+yo);





 
}

}



%>


?>


list.j$
========

<JDollar>

<USE> <WEB>.util;
<USE> Security;

<USE>  CUTIL;


<PACK> Program5
{
  
    <CLASS> Prog
   {

  
      public void Main()
      {


      
 
wdbaconn.JSTARWDBAQUERY("datastores", "USEDATABASE", "dbpwds", "C:\\Programs\\WNOSQL\\WNOSQLProgramfiles\\WNOSQL-cod"); 



 wdbaconn.JSTARWDBAUSERQUERY("dbuser", "dbpwds", "wilmix78", "wilmix78"); 




String  qh2="SELECTRVAL from electricitybill 7 to 24 , 1 to 5 ?= A By 1 1 : {0} : {0} :{0}";

  wdbaconn.WDBAQUERY(qh2);

ArrayLinearList x =  new ArrayLinearList();     


<TRY>
{


String s=Secure.RetreiveSecure("output.wdba" ,0); //retrieve  the  query  output   from   wdba file

s=s.Replace("[","").Replace("]","");




string []ename = s.Split(' ');
       

int lengthA = ename.Length;


<PRINTLN>(" <html>");
<PRINTLN>(" <form>");
<PRINTLN>(" <Table  bgcolor=gold>");
  <PRINTLN> ("Electricity customers...");

<PRINTLN> ("<BR>********************");


                 



int c=0;
  

     
    

for  (int  i=7;i<lengthA;i+=1)
{




 //<PRINTLN>(" <td>");


                      
                      //    <PRINTLN> (" <td>"+ename[i].Replace(",","").Replace("%2F","/").Replace("%40","@").Replace("+"," ")+"</td>");


                           
              // <PRINTLN>(" </td>");


x.add(c,ename[i].Replace(",","").Replace("%2F","/").Replace("%40","@").Replace("+"," "));





c++;
}

       

     
  
        
       
        
         


<PRINTLN>(" </table>");

<PRINTLN>(" </form>");
<PRINTLN>(" </html>");

       
   
      // output using an iterator
      Iterator y = x.iterator();
      while (y.hasNext())
         <PRINTLN>(y.next() + " ");



    Environment.Exit(-1);     

}

<CATCH>(<EXE> e)

{



}



		
}


}

}


Jquerytest.j$
==============


<JDollar>

<USE> <WEB>.util;
<USE> Security;

<USE>  CUTIL;


<USE> CDollar.WDBA; 
<USE> WDBA; 


<PACK> Program5
{
  
    <CLASS> Prog
   {


static string name, consumerId, consumerType;
        static double pressure = 5.5;
       


        public static void totalBill(double consumerUnit)
        {

           
            double Month =( pressure * consumerUnit) * 1;

<PRINTLN>("<td height=200 bgcolor=white>  <font size=4 color=blue>"+ Month+"/-</font></td>");
            
           
           
        }



  
      public void Main()
      {

ArrayList arm1= new ArrayList();

arm1.add("Sno");
arm1.add("Lno");
arm1.add("Billdetails");
arm1.add("Units");

arm1.add("NOT");

<PRINTLN>("<HTML>");

<PRINTLN>("<head> <style>");


<PRINTLN>("table, th, td {");
   <PRINTLN>(" border: 1px solid black; ");
<PRINTLN>("}");
<PRINTLN>("</style>");
<PRINTLN>("</head>");


<PRINTLN>("<BODY bgcolor=pink>");

<PRINTLN>("<form>");
 

  

ArrayList  armg= Request.Query(arm1,"electricitybill.cl.dsn",4,1);

string  s=armg.get(0).ToString();

 <PRINTLN>("<table style='width:100%;'cellpadding=10 cellspcing=5 bgcolor=gold >");

<PRINTLN>("<tr>");

<PRINTLN>("  <p align=center><font size=6 color=blue>TAMILNADU  ELECTRIC  SUPPLY UNIT</font></p> ");
  
<PRINTLN>("  <p align=center><font size=3 color=red>ELECTRIC  SUPPLY RECEIPT</font></p> "); 

<PRINTLN>(" <p align=left><font size=3 color=blue>Name:</font> </p><p align=right><font size=3 color=blue>SNO:"+s+"</font></p>"); 
<PRINTLN>("<p align=left><font size=3 color=blue>Electricity No:</font></p>"); 
<PRINTLN>("<p align=left><font size=3 color=blue>Receipt NO:</font></p><p align=right><font size=3 color=blue>DAY:</font></p>"); 
<PRINTLN>("</tr>");

  <PRINTLN>("<tr>");



<PRINTLN>(" <th><font size=4 color=blue> LNO </font></th>");
  
<PRINTLN>(" <th><font size=4 color=blue> BILL DETAILS</font></th>");
  
<PRINTLN>(" <th><font size=4 color=blue> UNITS </font></th>");
  
<PRINTLN>("<th> <font size=4 color=blue> Amount(Rs)</font></th>");


   
<PRINTLN>(" </tr>");
   
<PRINTLN>(" <tr>");


<PRINTLN>(" </tr>");
 
<PRINTLN>(" <tr>");

<PRINTLN>(" <td height=200  bgcolor=white><font size=4 color=blue> "+armg.get(1).ToString()+"</font></td>");
  
<PRINTLN>("<td height=200 bgcolor=white><font size=4 color=blue>"+armg.get(2).ToString().Replace("%40++","@").Replace("%2F","/").Replace("+"," ")+"</font></td>");
  
<PRINTLN>(" <td height=200 bgcolor=white><font size=4 color=blue> "+armg.get(3).ToString()+" units</font></td>");

double units =Convert.ToDouble(armg.get(3).ToString());
totalBill(units);
  


<PRINTLN>(" </tr>");
   
<PRINTLN>(" </tr>");
   
<PRINTLN>(" <tr>");


<PRINTLN>(" </tr>");
 
 
  
<PRINTLN>("</table>");

  <PRINTLN>("<br>");
  <PRINTLN>("<br>");
  <PRINTLN>("<br>");
  <PRINTLN>("<br>");
  <PRINTLN>("<br>");
  <PRINTLN>("<br>");


<PRINTLN>("<br>");
  <PRINTLN>("<br>");
  <PRINTLN>("<br>");
  <PRINTLN>("<br>");
  <PRINTLN>("<br>");
  <PRINTLN>("<br>");



<PRINTLN>("</form>");

<PRINTLN>("<p align=right><font size=3 color=blue>Electricity  accountant  Signature</font></p>"); 



<PRINTLN>("</html>");
      
 


String g = WDBASQL.WDBASQLS("datastores", "USEDATABASE", "dbpwds", "C:\\Programs\\WNOSQL\\WNOSQLProgramfiles\\WNOSQL-cod");

           


          String   t = WDBASQL.WDBASQLS("dbuser", "dbpwds", 1, "wilmix78", "wilmix78", 1, 5, g);



//String q = "CREATETABLE from electricitybill 0 to 0 , 1 to 5 ?= 6639 By 6639 f(x) : {SNO,LNO,BILLDETAILS,UNITS}: {} :{2,4}";

  //wdbaconn.WDBAQUERY(q);




Char  c= ' ';

ArrayList  datas1=WDBASQL.Query("TABLESIZE()","electricitybill","0",null,19,"","", null,"",0,"","",c,null,t,1,5);



String t1="";

t1=armg.get(0).ToString()+","+armg.get(1).ToString()+","+armg.get(2).ToString()+","+armg.get(3).ToString();

String  s12 ="INSERTINTO from electricitybill 0 to "+datas1.size()+" , 1 to 5 ?= A By 1 1 : {0} : {"+t1+"} : {0}";


  wdbaconn.WDBAQUERY(s12);







		
}


}

}


BILL.html
=============
<html>
  <head>
    <title>Electricity Bill Calculation</title>
    <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  
<style>
form {
    border: 3px solid #f1f1f1;
}

input[type=text], input[type=password] {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    box-sizing: border-box;
}

button {
    background-color: #4CAF50;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    cursor: pointer;
    width: 100%;
}

button:hover {
    opacity: 0.8;
}

.cancelbtn {
    width: auto;
    padding: 10px 18px;
    background-color: #f44336;
}

.imgcontainer {
    text-align: center;
    margin: 24px 0 12px 0;
}

img.avatar {
    width: 40%;
    border-radius: 50%;
}

.container {
    padding: 16px;
}

span.psw {
    float: right;
    padding-top: 16px;
}

/* Change styles for span and cancel button on extra small screens */
@media screen and (max-width: 300px) {
    span.psw {
       display: block;
       float: none;
    }
    .cancelbtn {
       width: 100%;
    }
}
</style>

  </head>

  <body class="fancy" bgcolor=pink>
<form action="http://localhost:8090/Jquerytest.j$" method="post" >



<div id="pageContainer">
     
      <div id="pageContent">

        <div id="chaptersAccordion">

            <h2><a href="#chapter1">ELECTRICITY BILL CALCULATION</a></h2>
            <div class="container">
              

<p>Enter  Your SNO: <input type="text" name="Sno" size="25" /></p>
<p>Enter your L.N.O : <input type="text" name="Lno" size="15"/></p>

<p>Kindly  Enter  Bill  Details : <input type="text" name="Billdetails" size="100"/></p>
<p>UNITS USED  : <input type="text" name="Units" size="15"/></p>




            </div>



             <div class="container" style="background-color:#f1f1f1">
              <input type="submit" name="CALCULATE" value="CALCULATE">
<input type="reset" name="Clear">
            </div>

 <div class="container" style="background-color:#f1f1f1">
         
<a href=http://localhost:8090/list.j$> Click here  to  view  ELECTRICITY BILL CUSTOMERS ...

            </div>



</form>

</body>
</html>

<BR><BR>
	
	
Advantages
============

=>It  saves  time  and  cost

=>It has  automatic  garbic  collection.


=>It  is  a  pure  oops  language.

=>It  is  a  Loosely  coupled  webapplication. ie)   C$WP

=>It  has   attraction  syntax.

=>Includes  all  advantages of  java

=>It  is  also   focused  for  enterprise  design

=>It  accepts   webassembly  format.
=> learnable   and  used  with J$
=> SAVES  time  and cost...

