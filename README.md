# signup
<!DOCTYPE html>
<!--[if lt IE 7]>      <html class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if IE 7]>         <html class="no-js lt-ie9 lt-ie8"> <![endif]-->
<!--[if IE 8]>         <html class="no-js lt-ie9"> <![endif]-->
<!--[if gt IE 8]>      <html class="no-js"> <!--<![endif]-->
<html>
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <title></title>
        <meta name="description" content="">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="">
    </head>
    <body>
        {% for message in messages  %}
        <div class = "alert alert- {{message.tags}} alert dismissable fade show" roles = "alert">
            <strong>Message:</strong>{{message}}
            <button type="button" class = "close" data-dismiss="alert" aria-label="Close">
            <span aria-hidden="true">&times;</span>
            </button>
        </div>
   {% endfor %} 

        <h3>SignUp</h3>
        <form action="/signup" method="post">
            {% csrf_token %}
            <label for="">Username</label>
            <input type="text" id="username" name ="username" placeholder="Create a user name (Only letters and numbers)" required>
            <br>
            <label for="">First Name</label>
            <input type="text" id="fname" name ="fname" placeholder="enter your firstname" required>
            <br>
            <label for="">Last name</label>
            <input type="text" id="lname" name ="lname" placeholder="enter your lastname" required>
            <br>
            <label for="">Emailadress</label>
            <input type="email" id="email" name ="email" placeholder="enter email" required>
            <br>
            <label for="">password</label>
            <input type="password" id="pass1" name ="pass1" placeholder="Createpass" required>
            <br>
            <label for="">Confirm password</label>
            <input type="password" id="pass2" name ="pass2" placeholder="confirmpass" required>
            <br>
            <button type="submit">Sign Up</button>
        </form>
        
        <script src="" async defer></script>
    </body>
</html>
