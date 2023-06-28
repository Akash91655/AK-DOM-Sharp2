<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
    <body>
        <form onsubmit="saveToLocalStorage(event)">
            <label> Name </label>
            <input type="text" name="username" required/>
            <label> EmailId </label>
            <input type="email" name="emailid" required/>
            <label>Phonenumber </label> 
            <input type="tel" name="phonenumber" />
            <button> Submit </button>
        </form>
        <script>
            function saveToLocalStorage(event) {
                event.preventDefault();
                const name = event.target.username.value;
                const email = event.target.emailid.value;
                const phonenumber = event.target.phonenumber.value;
                localStorage.setItem('name', name);
                localStorage.setItem('email', email);
                localStorage.setItem('phonenumber', phonenumber);
                const obj = {
                    name,
                    email,
                    phonenumber,
                }
                localStorage.setItem('userDetails', JSON.stringify (obj));
            }
        </script>
    
</body>
</html>
