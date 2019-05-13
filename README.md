# AharyLogistics.co.il


<!--  ----------------------------------------------------------------------  -->
<!--  NOTE: Please add the following <META> element to your page <HEAD>.      -->
<!--  If necessary, please modify the charset parameter to specify the        -->
<!--  character set of your HTML page.                                        -->
<!--  ----------------------------------------------------------------------  -->

<META HTTP-EQUIV="Content-type" CONTENT="text/html; charset=UTF-8">

<!--  ----------------------------------------------------------------------  -->
<!--  NOTE: Please add the following <FORM> element to your page.             -->
<!--  ----------------------------------------------------------------------  -->



<form name="myForm" action="https://webto.salesforce.com/servlet/servlet.WebToCase?encoding=UTF-8" onsubmit="return validateForm()" method="POST">

<input type=hidden name="orgid" value="00D4J000000FEEv">
<input type=hidden name="retURL" value="http://www.aharai.org.il/">

<!--  ----------------------------------------------------------------------  -->
<!--  NOTE: These fields are optional debugging elements. Please uncomment    -->
<!--  these lines if you wish to test in debug mode.                          -->
<!--  <input type="hidden" name="debug" value=1>                              -->
<!--  <input type="hidden" name="debugEmail" value="hen_9990@walla.com">      -->
<!--  ----------------------------------------------------------------------  -->



<body>

<script>
function validateForm() {
  var Fullname = document.forms["myForm"]["name"].value;
  var email = document.forms["myForm"]["email"].value;
  var subject = document.forms["myForm"]["subject"].value;
  var description = document.forms["myForm"]["description"].value;
  
  if (Fullname == "") {
    alert("Name must be filled out");
    return false;
  }
  if (/\S+@\S+\.\S+/.test(email)==false) {
    alert("Email is invalid");
    return false;
  }  
  if (subject == "") {
    alert("Ypu must choose a subject");
    return false;
  }  
  if (description == "") {
    alert("You must write a description");
    return false;
  }   
  
}
</script>

<script>
// Put this script in header or above select element
    function check(elem) {
        // use one of possible conditions
        // if (elem.value == 'Other')
        if (elem.selectedIndex == 2) {
            document.getElementById("other-div").style.display = 'block';
        } else {
            document.getElementById("other-div").style.display = 'none';
        }
    }
</script>


<style>
body {background-color: #ffffe6;font-family:verdana;
}

</style>
<head>
<center>
  <h1>Open A New Case</h1>
  </center>
</head>
<label for="name" > <font size="4">* Full Name: </label> <br>
<input  id="name" maxlength="80" name="name" size="20" type="text" /><br>
<br>
<label for="email"> * Email:</label><br>
<input  id="email" maxlength="80" name="email" size="20" type="text" /><br>
<br>
<label for="phone">Phone</label><br>
<input  id="phone" maxlength="40" name="phone" size="20" type="text" /><br>
<br>
<label for="subject">* Subject</label><br>
<select  id="subject" name="subject" onChange="check(this);">
<option value="">--None--</option>
<option value="Other"> <font size="4">New</option>
<option value="Car Related">Car Related</option>
<option value="Payment Related">Payment Related</option>
<option value="Event Related">Event Related</option>
</select><br>
<br>


<div id="other-div" style="display:none;">
        <label>Car number involved</label><br>
        
		<input  id="00N4J0000071zDp" name="00N4J0000071zDp" size="20" type="text" /><br>
        </label>

</div>


<label for="description">* Description</label><br>
<textarea name="description"></textarea><br>
<br>


<center>
<img src="https://pbs.twimg.com/profile_images/1207337583/___________.jpg"></center>
<center>
<input type="submit" name="submit" >
<input type="reset">
<h4> לחץ על שלח על מנת לפתוח קריאת שירות חדשה ועל אפס על מנת למחוק את כל השדות שהוזנו</h4>
</center>

</body>
</form>
