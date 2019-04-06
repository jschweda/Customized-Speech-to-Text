---?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Auf den Mund geschaut…]

## Auf den Mund geschaut…
### Customized Speech to Text

@snap[south-west span-60]
Jan Schweda
@snapend

@snap[south-east span-60]
@jschweda
@snapend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Agenda]

@snap[west span-45]
# Agenda
@snapend

@snap[north-east span-60 fragment]
@box[bg-green text-white box-narrow-padding](Warum?#Warum sollte Inklusion ein Thema für mich sein?)
@snapend

@snap[east span-60 fragment]
@box[bg-green text-white box-narrow-padding](Wie?#Verstanden! Aber wie fange ich an?)
@snapend

@snap[south-east span-60 fragment]
@box[bg-green text-white box-narrow-padding](Und dann?#Ok, ganz nett. Aber wie geht es weiter?)
@snapend

---?color=#303030&image=logo.png&position=right 10px top 10px&size=5%

@title[Warum]
@snap[center]
# Warum?
@snapend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Was zum schmunzeln]
@snap[north-west]
### Was zum schmunzeln
@snapend

<iframe width="900" height="500" src="https://www.youtube.com/embed/IKZToY-V16w" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Wer braucht das?]
@snap[north-west]
### Wer braucht das?
@snapend

@ul
- 800.000 Stotterer in Deutschland
- 100.000 Menschen mit aphasischer Störung
- Audiogen bedingte Sprechstörungen
- Menschen mit starkem Dialekt
- Kinder
@ulend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Conversational UI]
@snap[north-west]
### Conversational UI
@snapend

@ul
- Wer stellt seinen Wecker noch per Hand?
- Wer nutzt Siri, Alexa oder Cortana?
- Wer hat eine Freisprechanlage im Auto?
- Wie wird Mobility as a Service funktionieren?
@ulend

---?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@snap[center]
# Wie?
@snapend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[custom acoustic Model]
@snap[north-west]
### *custom acoustic Model* 
@snapend

@ul
- Nebengeräusche 
  - Auto 
  - Werkstatt
- Spezielle Aussprache
@ulend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Eigenes akustisches Modell]
@snap[north-west]
### Warum CRIS 
@snapend

@ul
- Nativer Azure Dienst
- Start mit wenig Daten möglich
- Qualität steigt mit der Anzahl der Datensätze
@ulend

@snap[south-west span-50]
[Unterstütze Sprachen](https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/language-support#speech-to-text)
@snapend

@snap[south-east span-50]
[Weiterlesen](https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/how-to-customize-acoustic-models)
@snapend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Workflow]
@snap[north-west span-40]
@box[bg-orange text-white box-wide-padding rounded](Aufnehmen @fa[arrows-h] Beschreiben)
@snapend

@snap[north-east span-40]
@box[bg-orange text-white box-wide-padding rounded](Hochladen)
@snapend

@snap[south-east span-40]
@box[bg-orange text-white box-wide-padding rounded](Trainieren)
@snapend

@snap[south-west span-40]
@box[bg-orange text-white box-wide-padding rounded](Benutzen)
@snapend

@snap[midpoint]
@fa[refresh fa-3x]
@snapend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
## Demo

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%

### Recording
@title[Recording]

[CRIS](cris.ai)

@ol
- Kommerzielle Tools
  - online
  - [Audacity](https://sourceforge.net/projects/audacity/)
- Eigener Code
@endol


Technische Anforderungen
WAV (RIFF) 
 sampling rate of 8 KHz or 16 KHz, and the sample values should be stored as uncompressed, pulse-code modulation (PCM) 16-bit signed integers (shorts).
Only single-channel (mono) audio files are supported.
The audio files can be between 100 microseconds and 1 minute in length, although ideally they should be around 10-12 seconds. Each audio file should ideally start and end with at least 100 microseconds of silence, and somewhere between 500 microseconds and 1 second is common.
If you have background noise in your data, we recommend that you also have some examples with longer segments of silence in your data—for example, a few seconds—before and/or after the speech content.
Each audio file should consist of a single utterance—for example, a single sentence for dictation, a single query, or a single turn of a dialog system.
Each audio file in the dataset should have a unique file name and a .wav extension.
The set of audio files should be placed in a single folder without subdirectories, and the entire set of audio files should be packaged as a single .zip-file archive.

Transcriptions for the audio dataset
The transcriptions for all WAV files should be contained in a single plain-text file. Each line of the transcription file should contain the name of one of the audio files, followed by the corresponding transcription. The file name and transcription should be separated by a tab (\t).


Transcription should be encoded as UTF-8 byte order mark (BOM).

The transcriptions are text-normalized so they can be processed by the system. However, there are some important normalizations that must be done by the user prior to uploading the data to the Custom Speech Service. For the appropriate language to use when you prepare your transcriptions, see Transcription guidelines for using the Speech Service.

Property	Value
File Format	RIFF (WAV)
Sampling Rate	8,000 Hertz (Hz) or 16,000 Hz
Channels	1 (mono)
Sample Format	PCM, 16-bit integers
File Duration	0.1 seconds < duration < 12 seconds
Silence Collar	> 0.1 seconds
Archive Format	.zip
Maximum Archive Size	2 GB



[Weiterlesen...](https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/prepare-transcription#other-languages)

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%

## Pflege
@title[Pflege]

[CRIS](cris.ai)

Data imports via the web portal are currently limited to 2 GB, so this is the maximum size of an acoustic dataset. This size corresponds to approximately 17 hours of audio that's recorded at 16 KHz or 34 hours of audio that's recorded at 8 KHz. The main requirements for the audio data are summarized in the following table:

acoustic models to choose from:

The Microsoft Search and Dictation AM model is appropriate for speech that's directed at an application, such as commands, search queries, or dictation.
The Microsoft Conversational Model is appropriate for recognizing speech that's spoken in a conversational style. This type of speech is usually directed at another person and occurs in a call center or meetings.
Latency for partial results in Conversational models is higher than in Search and Dictation models.

---?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@snap[center]
# Und dann?
@snapend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[API]
@snap[north-west]
### API 
@snapend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Integration]
@snap[north-west]
### Integration 
@snapend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Linguistische Modelle]
@snap[north-west]
### Linguistische Modelle 
@snapend

@snap[south]
[docu](https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/how-to-customize-language-model)
@snapend
+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Fragen]
@snap[north-west]
### Fragen 
@snapend

+++?color=#303030&image=logo.png&position=right 10px top 10px&size=5%
@title[Danke]
@snap[north-west]
### Danke 
@snapend

+++?image=logo.png&size=50%

