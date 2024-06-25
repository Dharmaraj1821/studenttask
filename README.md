# studenttask
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Js Task - 2</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC" crossorigin="anonymous">
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384-IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/js/bootstrap.min.js" integrity="sha384-cVKIPhGWiC2Al4u+LWgxfKTRIcfu0JTxR+EQDz/bgldoEyl4H0zUF0QKbrJ0EcQF" crossorigin="anonymous"></script>
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css" integrity="sha512-SnH5WK+bZxgPHs44uWIX+LLJAJ9/2PkPKZ5QiAj6Ta86w+fsb2TkcmfRyVX3pBnMFcV7oQPJkl9QevSCWr3W6A==" crossorigin="anonymous" referrerpolicy="no-referrer" />
<script>
    function load(id)
      {
        if(id=='studentName'){
            document.getElementById('studentRollNo').style.background="none";
        }else{
            document.getElementById('studentName').style.background="none";
        }
        document.getElementById(id).style.background="green";
      }
      function formValidation()
      {
        const studentName=document.forms.studentData.studentName.value;
        const studentRollNo=document.forms.studentData.studentRollNo.value;
        if (studentName === "" || studentName.includes('0') || studentName.includes('1') || studentName.includes('2') || name.includes('3')
        || studentName.includes('4') || studentName.includes('5') || studentName.includes('6') || studentName.includes('7')
        || studentName.includes('8') || studentName.includes('9')) {
            window.alert("Please enter your name properly.");
            document.getElementById('studentName').focus();
            return false;
        }
        if (isNaN(studentRollNo)) {
            window.alert("Please enter Numeric value");
            document.getElementById('studentRollNo').focus();
            return false;
        } else {
            window.alert("Numeric value is: " + studentRollNo);
        }
      }
</script>
</head>
<body>
    <div class="container">
        <form name="studentData" >
            <div class="row">
                <div class="col-4"><label>Student Name</label><input type="text" name="studentName" id="studentName" onfocus="load('studentName')" class="form-control inputField"></div>
                <div class="col-4"><label>Student Roll No</label><input type="text" name="studentRollNo" id="studentRollNo" onfocus="load('studentRollNo')" class="form-control inputField"></div>
                <div class="col-4 mt-4"><input type="button" onclick="formValidation()" value="Submit" class="btn btn-success"></div>
            </div>
        </form>
    </div>
</body>
</html>

