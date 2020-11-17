# pixelPusherCannedFileTutorial
Here is a CLEAR tutorial of how to create the canned show file for pixelpusher [english and french]

FRENCH

L'idée est d'enregistrer une animation lorsqu'elle est envoyée en réseau vers le pixelpusher
elle est stockée dans un petit fichier nommé "canned show file", qu'il faudra placer dans la clé usb et reset le pixelpusher

- installer processing, et importer la librairie pixelpusher.
- Ouvrir un fichier exemple, dans Fichier -> Examples -> Contributed Librairies -> PixelPusher -> 
- Pour ce tuto, nous ouvrirons pixelpusher_example
- Se placer sur le même réseau que le pixelpusher, appuyer sur play, et voir si tout fonctionne bien
- normalement, en bougeant la souris sur la fenetre qui s'est ouverte, les couleurs qui apparaissent sont censées etre liées avec celles des led du pixelpusher. Appuyer sur stop.

- Comme tout foncitonne bien, ajouter cette ligne en en-tête : 
    import com.heroicrobot.dropbit.devices.pixelpusher.PixelPusher;

- un peu plus bas, en dessous de cette ligne : "List<Strip> strips = registry.getStrips();", aujouter ces deux lignes : 
List<PixelPusher> pushers = registry.getPushers();
pushers.get(0).startRecording("cannedfile.dat");

- Appuyer sur play, puis faire lapetite animation à la souris
- quand c'est fini, appuyer sur stop
- un fichier cannedfile.dat est apparu juste a côté de processing.exe
- brancher la clé usb du pixelpusher sur l'ordinateur
- copier el fichier dedans et le renommer en "canned.dat"
- ouvrir le fichier "pixel.rc" avec un éditeur de texte et écrire à la fin "canned_file=1"
- enregistret, éjecter la clé, la placer dans le PP, le reseter et VOILA

ENGLISH

The idea is to record an animation when it is sent over the network to the pixelpusher
it is stored in a small file named "canned show file", which must be placed in the usb key and reset the pixelpusher

- install processing, and import the pixelpusher library.
- Open an example file, in File -> Examples -> Contributed Libraries -> PixelPusher ->
- For this tutorial, we will open pixelpusher_example
- Go to the same network as the pixelpusher, press play, and see if everything works well
- normally, by moving the mouse over the window that opened, the colors that appear are supposed to be linked with those of the pixelpusher leds. Press stop.

- As everything works well, add this line in the header:
    import com.heroicrobot.dropbit.devices.pixelpusher.PixelPusher;

- a little lower, below this line: "List <Strip> strips = registry.getStrips ();", add these two lines:
List <PixelPusher> pushers = registry.getPushers ();
pushers.get (0) .startRecording ("cannedfile.dat");

- Press play, then do the little animation with the mouse
- when it's finished, press stop
- a cannedfile.dat file appeared right next to processing.exe
- connect the pixelpusher usb key to the computer
- copy the file inside and rename it to "canned.dat"
- open the file "pixel.rc" with a text editor and write at the end "canned_file = 1"
- save, eject the key, place it in the PP, reset it and VOILA
