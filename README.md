# atelier-mm

```
from pydub import AudioSegment
```

## Défis
- http://ressources.magicmakers.fr/ressources-python-defis-creations/

## Ressources
- http://ressources.magicmakers.fr/ressources-python-bases-pydub/
- http://ressources.magicmakers.fr/ressources-python-bases-pydub/

## Doc de AudioSegment

mon_son.**apply_gain**(volume): applique un gain de "volume" (un nombre décimal) à mon_son et renvoie la piste modifiée
```
song = AudioSegment.from_file("my_song.mp3", format = "mp3")
forte = song.apply_gain(10) #attention aux oreilles!
```

**export**("fichier_de_destination.type", format="type"): sauvegarde la piste dans un fichier
```
song = AudioSegment.from_file("my_song.mp3", format = "mp3")
# modifications diverses
song.export("my_custom_song.mp3", format = "mp3")
```

mon_son.**fade_in**(duration): fait un fade in sur duration ms en début de piste et la renvoie modifée
```
musique = AudioSegment.from_file("musique.mp3", format="mp3")
fade_in = musique.fade_in(10000)
```

mon_son.**fade_out**(duration): fait un fade out sur duration ms en fin de piste et la renvoie modifée
```
musique = AudioSegment.from_file("musique.mp3", format="mp3")
fade_out = musique.fade_out(10000)
```

**from_file**("nom_fichier.type", format="type"): importe un son et le stocke dans une variable
```
song = AudioSegment.from_file("my_song.mp3", format = "mp3")
```

mon_son.**overlay**(autre_son): superpose la piste autre_son au dessus de mon_son et la stocke dans une nouvelle variable
```
piste_1 = AudioSegment.from_file("song1.mp3", format = "mp3")
piste_2 = AudioSegment.from_file("sound2.mp3", format = "mp3")
nouvelle_piste = piste_1.overlay(piste_2)
```

**reverse**(): inverse la piste et la stocke dans une nouvelle variable
```
inverse = AudioSegment.from_file("my_song.mp3", format = "mp3")
musique = inverse.reverse()
```

**speedup**(ma_piste, playback_speed=1.5): acceler la piste et la stocke dans une nouvelle variable. Par défault, playback_speed vaut 1.5
```
normal = AudioSegment.from_file("normal.mp3", format = "mp3")
fast = AudioSegment.speedup(normal)
faster = AudioSegment.speedup(normal, playback_speed = 4)
```

**silent**(duration=1000): créé un silence de longueur "duration" ms. par défaut, 1000 ms
```
silence_1s = AudioSegment.silent()
silence_10s = AudioSegment.silent(duration = 10000)
```
