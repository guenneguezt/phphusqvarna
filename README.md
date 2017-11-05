# phphusqvarna
Control your Husqvarna automower using Automower connect API.

# Requirements
  + php 5.x
  + curl

# One way to configure the environment to run phphusqvarna

include the husqvarna_api.class.php file in your own script.
require_once("husqvarna_api.class.php");

# Commands
## Instantiate a class
$session_husqvarna = new husqvarna_api();

## Connect
    $session_husqvarna->login($account, $passwd);

## List yours automower
    $robots = $session_husqvarna->list_robots();

## Read status of your automower
    $status = $session_husqvarna->get_status("1708XXXX-17013YYYY"):

## Read the geo position of the automower
    $position = $session_husqvarna->get_geofence("170811841-170130242"):

## Send a commande to your automower
    $session_husqvarna->control("1708XXXX-17013YYYY", 'START'):
	The commande can be PARK, STOP, START

## Logout
    $session_husqvarna->logout();

# Warning
The API and command line are not stable and can change at any time.

# Special Thanks
chrisz ([@chrisz](https://github.com/chrisz))
