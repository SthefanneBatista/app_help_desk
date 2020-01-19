Documentation: 

<?php

//Confirm login

//Here we create an array with two "values", the email and the password,
//first of all, i have been add at the array some test values, 
//just to see with was all fine in the logic, not considering the bd

$user_verified = false;


$users_app = array(
    array('email' => 'adm@test.com.br', 'password' => '123456'),
);

foreach($users_app as $user){

if($user['email'] == $_POST['email'] && $user['password'] == $_POST['password']){

    $user_verified = true;
    }
}

if($user_verified){

} else{
    header('Location: index.php?login=erro')
}

?>


//The user tried to login in the app, but the email/password are invalid
//So now, back to the index, and show to the user there is something wrong
//A simple and direct line of code just to show the message
<? if(isset($_GET['login']) && $_GET['login'] == 'erro') { ?>
          
              <div class="text-danger"> 
                Usuário ou senha inválido(s)
            </div>
          
              <? } ?>


-----------------------------------------------------------------


