# node pour flux video
<p>Serveur node permettant à la carte arduino d'envoyer un flux vidéo et à l'application mobile d'ouvrir des sockets de lecture</p>
# groupe 1
<p>Loïs Lachaud, Baptiste Lanusse, Yoann Murat, Alexandre Plaitant</p>
<p>Cours IOT - Ingésup Bordeaux - 2016/2017</p>
<br/>
----------------------------------------------------------------------
<br/>
<p>Possibilité d'envoyer un port pour le socket et un port pourt le flux vidéo.</p>
<p>Par défaut, le flux vidéo est à envoyer sur le port 8082 et le socket à récupérer sur le port 8084</p>
<p>ffmpeg a été ajouté à la carte arduino afin d'envoyer le flux vidéo, et la commande exécutée est la suivante:</p>
<p>"ffmpeg -s 160x120 -f video4linux2 -i /dev/video0 -r 20 -f mpeg1video -ab 128k -r 20 http://192.168.43.239:8082/pass/160/120"</p>
