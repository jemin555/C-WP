# C$WP
============

C$WP   stands    for  a    Loosely coupled   remoteweb/web application   focussed  for  CDollar  Professionals for  Mobile web/remoteweb  application. it  is   invented  by  wilmix  jemin j .


SYNTAX
======



<?language=C$> //indicates   that  remote  /webapplication   for   mobiles   using  cdollar



<IMPORT>  java.util.*; //load  cdollar  java util packages.
 

<%




public class <Classname> {


  public void main() // main function  of  C$
{


//loosely  coupling  using  C$

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

HTML.displayhtml("Register.html");

//loosely  coupling  using  C$

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


Register.html
=============

<html>
  <head>
    <title>STUDENT  REGISTRATION</title>
    
  </head>

  <body class="fancy">
<form action="http://localhost:8090/Programs11.exe" method="post" >
  
  //include  oakjava7  file  or  j$  file

<div id="pageContainer">
     
      <div id="pageContent">

        <div id="chaptersAccordion">

            <h2><a href="#chapter1">Enter your   Details</a></h2>
            <div>
              

<p>Enter  Your Name: <input type="text" name="name" size="25" /></p>
<p>Enter your Username : <input type="text" name="uname" size="15"/></p>
<p>Enter  the password : <input type="password" name="password" size="25" /></p>
<p>Choose your  state  : <input type="text" name="state" size="15"/></p>
<p>Choose  your  Country  : <input type="text" name="country" size="15"/></p>

<p>Enter  the   password : <input type="password" name="spwd" size="25" /></p>
<p>Enter your secret  password text : <input type="text" name="stext" sixe="15"/></p>

<p>Enter  your family details : <input type="text" name="familydet" size="25" /></p>

<p> Enter  Percentage of  marks  scored <input type="text" name="Indent" sixe="5"/></p>

<p>Enter Your Favourite subject <input type="text" name="CIndent" size="15"/></p>


            </div>


<h2><a href="#chapter2">REGISTER</a></h2>
            <div>
              <input type="submit" name="Click">
<input type="reset" name="Clear">
            </div>


</form>

</body>
</html>

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

