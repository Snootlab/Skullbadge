=========================================================================================
     _______..__   __.   ______     ______   .___________. __          ___      .______   
    /       ||  \ |  |  /  __  \   /  __  \  |           ||  |        /   \     |   _  \  
   |   (----`|   \|  | |  |  |  | |  |  |  | `---|  |----`|  |       /  ^  \    |  |_)  | 
    \   \    |  . `  | |  |  |  | |  |  |  |     |  |     |  |      /  /_\  \   |   _  <  
.----)   |   |  |\   | |  `--'  | |  `--'  |     |  |     |  `----./  _____  \  |  |_)  | 
|_______/    |__| \__|  \______/   \______/      |__|     |_______/__/     \__\ |______/  
                                                                                          
=========================================================================================
Infos : snootlab.com
Contact : contact@snootlab.com
Questions : forum.snootlab.com




============ GUIDE DE PROGRAMMATION DU ZOMBADGE ============

Mat�riel n�cessaire :
- Arduino	(x1)
- C�bles	(x6)
- Zombadge	(x1)	


Sch�ma de c�blage pour programmer le Zombadge : 
http://forum.snootlab.com/viewtopic.php?f=35&t=122


1/ D�compresser les fichiers pr�sents dans l'archive que vous venez de t�l�charger dans un r�pertoire

2/ Programmer la carte Arduino en programmateur ISP en s�lectionnant l'exemple "ArduinoISP" (Menu File\Examples\ArduinoISP)
Puis uploader le sketch dans l'Arduino (bouton Upload) apr�s avoir s�lectionn� l'Arduino correspondant dans le Menu Tools\Boards

V�rifier le num�ro de port COM affect� � l'Arduino (Menu Tools\Serial Port)

3/ �teindre et retirer la pile du Zombadge
Op�ration obligatoire, vous risquez d'endommager la pile et le circuit si l'interrupteur passait sur "on" lors de la manipulation.

4/ Relier le Zombadge � l'Arduino comme indiqu� sur le sch�ma et la photo ci-dessous
(connecteur ISP sur le Zombadge not� ISP, le point en haut � droite sert de d�trompeur)

5/ Ouvrir un terminal ("invite de commande"), se rendre dans le r�pertoire o� vous avez d�compress� les fichiers � l'�tape 1

6/ Editer le fichier Makefile et modifier la ligne 4 ("AVRDUDE_PORT = COM16") avec le port COM qui a �t� affect� par Arduino � votre carte (�tape 2), enregistrer la modification

7/ Dans le terminal ex�cuter "make survivor ID=xx" avex xx un nombre compris entre 1 et 149 inclus, diff�rent pour chaque badge,
puis attendre que le programme s'ex�cute. ATTENTION ! 0 ne dois pas �tre utilis�. Jamais. C'est une ID r�serv�e.

8/ D�brancher tous les c�bles

9/ Remettre la pile du Zombadge

10/ C'EST PARTI !!




============ PROGRAMMING THE ZOMBADGE (English) ============

Hardware needed :
- Arduino	(x1)
- Cables	(x6)
- Zombadge	(x1)		


Wiring schematic to program the Zombadge : 
http://forum.snootlab.com/viewtopic.php?f=35&t=122


1/ Uncompress the files presents in the zip archive in the desired directory

2/ Program the Arduino board in ISP programmer mode by selecting the example "ArduinoISP" in the Arduino IDE (Menu File\Examples\ArduinoISP)
Then upload the sketch in the Arduino (Upload button) after have selected your board in the Menu Tools\Boards

Check the COM port number assigned to the Arduino (Menu Tools\Serial Port)

3/ Shutdown the Zombadge then remove his battery
If you ommit to do this, you can seriously damage the battery et the circuit if the switches accidentaly is put on "On" position during programming

4/ Wire the Zombadge to the Arduino as indicated on the forum link above
(the dot on the top-right corner of the ISP connector is used as a polarizing slot)

5/ Open a terminal (Command line interface), select the directory where you've uncompressed the archive in the step 1 as your working directory

6/ Edit the Makefile and modify the line 4 ("AVRDUDE_PORT = COM16") with the port COM number found during the step 2, then save the file

7/ In the terminal run "make survivor ID=xx", with xx a number between 1 and 149, different for each badge,
 and wait until the programming session ends. WARNING ! 0 should not be used. Never. It's a reserved ID.

8/ Unplug all the cables

9/ Put the battery in the Zombadge

10/ GO PLAY GAME !!