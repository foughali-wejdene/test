<!DOCTYPE html>
<html lang="fr">

<head>
  <title>RESILIENCE 34</title>
  <!-- <link rel="stylesheet" href="/mdl/1.2.0/material.teal-amber.min.css" /> -->
  <!-- <link rel="stylesheet" href="/mdl/1.2.0/material.blue_grey-green.min.css" /> -->
  <!-- Feuille de style -->
  <link rel="stylesheet" href="/mdl/1.3.0/material.blue_grey-green.min.css" />
  <link rel="stylesheet" href="/mdl/fonts/roboto.css">
  <link rel="stylesheet" href="/css/style.css" />
  <link href="/mdl/material-icons/material.css" rel="stylesheet" />
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
  <script src="https://pagination.js.org/dist/2.1.4/pagination.min.js"></script>

<style type="text/css">
  input[type=text], input[type=password] {
  width: 50%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}
input[type=submit] {
  width: 50%;
  color: white;
  padding: 12px 18px;
  margin: 0 5px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
.mdl-layout__drawer {
      min-width: 240px !important;
      /* max-width: 30% !important; */
      width: auto !important;
      left: -100%;
    }

    .mdl-layout__drawer.is-visible {
      left: 0;
    }

    .img-rounded {
      border-radius: 50%;
      border: 2px solid white;
    }

    .user-badge b {
      font-size: 14px;
      font-weight: 100;
      margin-right: 15px;
      line-height: 36px;
      float: left;
    }

    .user-badge span {
      width: 36px;
      height: 36px;
      display: inline-block;
      border-radius: 50%;
      background: green;
      position: relative;
    }

    form .mdl-card {
      text-align: center;
      width: 100%;
    }

    .user-badge span i {
      position: absolute;
      top: 5px;
      left: 6px;
      cursor: pointer;
    }

    .mdl-menu__container.is-visible,
    .mdl-menu__container.is-animating {
      margin-top: 5px;
    }

    main.mdl-layout__content {
      /*background-image: url("/img/industry.jpg");*/
    }

    .mdl-layout__drawer-button .material-icons {
      line-height: 1.7;
    }

    .mdl-textfield--floating-label.is-focused .mdl-textfield__label,
    .mdl-textfield--floating-label.is-dirty .mdl-textfield__label,
    .mdl-textfield--floating-label.has-placeholder .mdl-textfield__label {
      color: #1976d2 !important;
    }

    .mdl-textfield__label:after {
      background-color: #1976d2;
    }

    body * {
      font-family: Roboto;
    }

    a.logout {
      text-decoration: none;
    }

    dialog[open] {
      -webkit-animation: show .45s ease normal;
    }

    @-webkit-keyframes show {
      from {
        transform: translateY(-110%);
      }

      to {
        transform: translateY(0%);
      }
    }

    dialog::backdrop {
      background: rgba(0, 0, 0, 0.5);
    }

    dialog {
      padding: 0;
    }

    .mdl-dialog {
      width: 50%;
    }

    .goodyear-color {
      background-color: #012d89 !important;
    }

    .goodyear-color--light {
      background-color: #2150af !important;
    }

    .mdl-layout__drawer-button {
      outline: none;
    }

    .goodyear-color-text {
      color: #FFDE00 !important;
    }

    .goodyear-color-all {
      background-color: #012d89 !important;
      color: #FFDE00 !important;
    }

    .mdl-navigation {
      padding-top: 0px !important;
    }

    .right {
      float: right;
    }

    .input-date {
      top: -3px;
    }

    .input-date>label {
      top: 7px;
    }

    .moderatorAdminManualButton {
      background-color: #e23737;
      color: #000000;
    }

    .userManualButton {
      background-color: #65ad48;
      color: #000000;
    }

    .developerManualButton {
      background-color: #666eda;
      color: #000000;
    }

    .cursorHand {
      cursor: pointer;
    }

    .cryo-color-text{
      color: #fdf5e6  !important;
    }



 </style>
</head>
<?php

	
    if(isset($_POST['login']) && isset($_POST['pwd'])){
        
        $server = "192.168.190.132";
        $port = 389;
        $domain = '@mspr.fr';
        $connection = $ldap = ldap_connect($server);
        if(!$connection){
        	exit('Connection failed !!!');
        }

        $login = $_POST['login'];
        $password = $_POST['pwd'];

        ldap_set_option($connection , LDAP_OPT_PROTOCOL_VERSION, 3);
        ldap_set_option($connection , LDAP_OPT_REFERRALS, 0);

        $bind = @ldap_bind($connection,$login.$domain,$password);

        if(!$bind){
        	exit('Binding failed!!!');
        }else{
            //echo 'hello from LDAP ' . $login ;
            echo "<script type='text/javascript'>document.location.replace('acceuil.php');</script>";

            ldap_close($connection);
            header('Location : ');
        }

       

     }else{
        ?>


<header class="mdl-layout__header goodyear-color">
      <!-- Menu complet en haut -->
      <div class="mdl-layout__header-row" style="height:60px">
        <span class="mdl-layout-title">
          <a id="main_title_goodyear" href="/"><img style="height:60px;width: 100px;" src="img/chatelet1.png" /></a>
          
          <sup style="font-size:18px; font-weight: bold; color:white;"><b>RESILIENCE 34</b></sup>
        </span>

      </div>
    </header>


<div class="mdl-cell mdl-cell--4-col"></div>
<form action="#" method="POST" class="mdl-cell mdl-cell--4-col">
  <div class="mdl-card mdl-shadow--8dp" style=" box-shadow: 6px 6px 6px grey; width: 40%;/* ta valeur */
margin: auto;">
    <div class="mdl-card__title goodyear-color--light" style="height:40px;">
      <h2 class="mdl-card__title-text mdl-color-text--white titreConnexion">Connexion</h2>
    </div>
    <br>
    <div class="mdl-card__supporting-text">
      <div class="mdl-textfield mdl-js-textfield mdl-textfield--floating-label mdl-cell mdl-cell--10-col login" autocomplete="off" style="margin-bottom: 25px;">
         <label class="mdl-textfield__label" for="login">Login</label><br>
        <input class="mdl-textfield__input" type="text" name="login" id="login" autocomplete="off" maxlength="30">
       
      </div>
      <div class="mdl-textfield mdl-js-textfield mdl-textfield--floating-label mdl-cell mdl-cell--10-col login" autocomplete="off">
        <label class="mdl-textfield__label" for="pwd">Password</label><br>
        <input class="mdl-textfield__input" type="password" name="pwd" autocomplete="off" id="pwd">
        <br>
      </div>
    </div>
    <br>
    <div class="mdl-card__actions mdl-card--border">
      <input type="submit" class="mdl-button mdl-js-button mdl-button--raised goodyear-color--light mdl-color-text--white valider" />
    </div>
    <br>
  </div>
</form>
<div class="mdl-cell mdl-cell--4-col"></div>

   <?php  }  ?>    
   
