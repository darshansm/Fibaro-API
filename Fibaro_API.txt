# Fibaro-API

Meaning of the variables:

<LOGIN> = The user authorized to perform the action (ex: admin)
<PASS> = Your password
<IP> = The IP address of your Home Center, it is therefore necessary to assign a fixed IP (via the lease cancellation of your box / Internet router)
<ID> = Z-Wave module identifier (how to find the ID of a module?)
name = action (ex: turnOff, turnOn, setValue)
<Value> = value (eg level of variation at 39% -> arg1 = 39)
Examples:

http: // <LOGIN>: <PASS> @ <IP> / api / CallAction deviceID = <ID> & name = setValue & arg1 = <VALUE>
... becomes:

http: // admin: mot_de_passe@192.168.1.5/api/callAction deviceID = 4 & name = turnoff
http: // admin: mot_de_passe@192.168.1.5/api/callAction deviceID = 7 & name = setValue & arg1 = 39
 

LIST OF API

Inverters
http: // <LOGIN>: <PASS> @ <IP> / api / CallAction deviceID = <ID> & name = setValue & arg1 = <VALUE>
  

ON / OFF (eg Wall Plug, FGS211, FGS221 micro-modules, etc.)
http: // <LOGIN> <PASS> @ <IP> / api / CallAction deviceID = <ID> & name = TurnOn?

http: // <LOGIN> <PASS> @ <IP> / api / CallAction deviceID = <ID> & name = turnoff?
 

Shutters
http: // <LOGIN>: <PASS> @ <IP> / api / CallAction deviceID = <ID> & name = setValue & arg1 = <VALUE>

http: // <LOGIN> <PASS> @ <IP> / api / CallAction deviceID = <ID> & name = setAjar?

http: // <LOGIN> <PASS> @ <IP> / api / CallAction deviceID = <ID> & name = stop?
 

FG-RGBW module
http: // <LOGIN> <PASS> @ <IP> / api / CallAction deviceID = <ID> & name = turnoff?

http: // <LOGIN> <PASS> @ <IP> / api / CallAction deviceID = <ID> & name = TurnOn?

 

http: // <LOGIN>: <PASS> @ <IP> / api / CallAction deviceID = <ID> & name = setColor & arg1 = <VALUE> & arg2 = <VALUE> & arg3 = <VALUE> & arg4 = <VALUE>

 

http: // <LOGIN>: <PASS> @ <IP> / API / callAction? deviceID = <ID> & name = startProgram & arg1 = <PROGRAM ID>
 

Virtual modules
ID = device ID
arg1 = button ID
arg2 = slider value (only for slider)

http: // <LOGIN>: <PASS> @ <IP> / API / callAction? deviceID = <ID> & name = pressButton & arg1 = <BUTTON ID>

http: // <LOGIN>: <PASS> @ <IP> / API / callAction? deviceID = <ID> & name = setSlider & arg1 = <SLIDER ID> & arg2 = <VALUE>
  

Scenes
ID = SceneID

http: // <LOGIN>: <PASS> @ <IP> / api / sceneControl? id = <SCENE ID> & action = start

http: // <LOGIN>: <PASS> @ <IP> / api / sceneControl? id = <SCENE ID> & action = stop
 

Danfoss Living Connect thermostatic heads
http: // <LOGIN>: <PASS> @ <IP> / API / callAction? deviceID = <ID> & name = setTargetLevel & arg1 = <TEMP VALUE>

http: // <LOGIN>: <PASS> @ <IP> / API / callAction? deviceID = <ID> & name = setTime & arg1 = <TIME VALUE>
Notifications
ID = Device (Iphone, e-mail and so on)
arg1 = Notification template
http: // <LOGIN> <PASS> @ <IP> / api / callActiondeviceID = 9 & name = & sendDefinedPushNotification arg1 = 1
  

"Energy" sign
http: // <LOGIN> <PASS> @ <IP> / api / energy / now-3600 / now / single / devices / power / 58
State and Value Retrieval by JSON Requests:
http: // <LOGIN> <PASS> @ <IP> / api / rooms
http: // <LOGIN> <PASS> @ <IP> / api / scenes
http: // <LOGIN> <PASS> @ <IP> / api / devices
http: // <LOGIN>: <PASS> @ <IP> / API / devices? id = 316 # Specific value of a device
http: // <LOGIN> <PASS> @ <IP> / api / virtualDevices
http: // <LOGIN> <PASS> @ <IP> / api / globalVariables
http: // <LOGIN> <PASS> @ <IP> / api / weather
http: // <LOGIN> <PASS> @ <IP> / api / sections
http: // <LOGIN> <PASS> @ <IP> / api / users
http: // <LOGIN> <PASS> @ <IP> / api / energy / now-3600 / now / single / devices / power / 58

etc.



