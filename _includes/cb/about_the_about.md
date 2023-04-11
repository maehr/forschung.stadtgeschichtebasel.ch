{% assign imagesample = site.data[site.metadata] | where_exp: 'item','item.format contains "image"' | first %}
{% capture imagesampleid %}{{imagesample.objectid | default: "https://www.lib.uidaho.edu/collectionbuilder/demo-objects/mg101_b6_photographs_01.jpg"}}{% endcapture %}
{% assign pdfsample = site.data[site.metadata] | where_exp: 'item','item.format contains "pdf"' | first %}
{% capture pdfsampleid %}{{pdfsample.objectid | default: "https://digital.lib.uidaho.edu/utils/getfile/collection/ui_ep/id/21768/filename/uiext21768.pdf"}}{% endcapture %}
{% assign videosample = site.data[site.metadata] | where_exp: 'item','item.format contains "video"' | first %}
{% capture videosampleid %}{{videosample.objectid | default: "https://cdil.lib.uidaho.edu/storying-extinction/objects/trailcams/videos/ballcreek-cedarrub-birdonpath.mp4"}}{% endcapture %}
{% assign audiosample = site.data[site.metadata] | where_exp: 'item','item.format contains "audio"' | first %}
{% capture audiosampleid %}{{audiosample.objectid | default: "https://www.lib.uidaho.edu/digital/mp3s/Clouds.mp3"}}{% endcapture %}

## Über die Über-Seite

Wir möchten die Erstellung ansprechender Interpretations-Seiten vereinfachen. CollectionBuilder gibt Ihnen daher Werkzeuge an die Hand, mit denen Sie *mit* Ihren Sammlungsinhalten schreiben können!

Die Vorlage enthält ein anpassbares Layout für die Seite "Über", das für lange Inhalte mit Rich-Media-Einbettungen konzipiert ist.
Die Inhalte werden in [Markdown](https://guides.github.com/features/mastering-markdown/) geschrieben und mit "Includes" erweitert, die Sammlungsinhalte, externe Medien und [Bootstrap](https://getbootstrap.com/) Funktionen wie Karten und Modals einbinden.
Wir hoffen, dass dies die Entwicklung der Sammlung UND das Hinzufügen interessanter und ansprechender Kontextinformationen für Website-Ersteller erleichtert. 

Jede "Include"-Datei hat mehrere Optionen, die in den Dateien selbst dokumentiert sind - kopieren Sie die Beispiele, um zu sehen, wie es mit Ihren Inhalten funktioniert! 
In der Demo unten haben wir die Anzeigebreiten auf 25% und 50% festgelegt, um Platz zu sparen, aber Sie können das gesamte Bild oder Dokument einbinden.

Auf unserer CollectionBuilder-GH-Demoseite sehen Sie auch eine Seite mit [einer Fülle von Feature-Include-Optionen] (https://collectionbuilder.github.io/collectionbuilder-gh/feature_options.html). 

{% include feature/button.html text="Feature *Includes* Bonanza-Seite" link="https://collectionbuilder.github.io/collectionbuilder-gh/feature_options.html" color="primary" size="lg" centered=true %}

### Sammlungselemente einbeziehen

Die Vorlage bietet Includes, mit denen Sie Ihre Sammlungsobjekte und Metadaten in Ihre Interpretationsseite einbinden können. So können Sie Ihre Materialien direkt in den Inhalt einbetten.

#### Ein Bild einbinden

- Bild --> `{% raw %}{% include feature/image.html objectid="demo_001" width="75" %}{% endraw %}`

{% include feature/image.html objectid=imagesampleid width="75" %}

#### Eine PDF einbinden

- PDF -- > `{% raw %}{% include feature/pdf.html objectid="demo_002" width="50" %}{% endraw %}`

{% include feature/pdf.html objectid=pdfsampleid width="50" %}

#### Ein Video einbinden

- Video: `{% raw %}{% include feature/video.html objectid="demo_004" %}{% endraw %}`

{% include feature/video.html objectid=videosampleid width="75" %}

#### Eine Audiodatei einbinden

- Audio: `{% raw %}{% include feature/audio.html objectid="demo_003" %}{% endraw %}`

{% include feature/audio.html objectid=audiosampleid %}

### Bootstrap-Funktionen einbinden

Die Vorlage enthält auch Includes, die das Hinzufügen von [Bootstrap](https://getbootstrap.com/) Komponenten zu Ihrem Markdown-Text erleichtern.
Mit diesen Funktionen können Sie Ihre Inhalte besser organisieren und hervorheben.

#### Eine Karte einbinden

- Karte -- > `{% raw %}{% include feature/card.html header="Dies ist eine Karte" text="Die Karte zeigt ein Bild aus der Sammlung als Cap" objectid="demo004" width="25" centered=true %}{% endraw %}`

{% include feature/card.html header="Dies ist eine Karte" text="Die Karte zeigt ein Bild aus der Sammlung als Kappe" objectid="demo_001" width="25" centered=true %}

#### Eine Schaltfläche einfügen 

- Schaltflächen -- > `{% raw %}{% include feature/button.html text="Schaltfläche Link zu Irgendwo" link="https://collectionbuilder.github.io/" color="success" %}{% endraw %}`

{% include feature/button.html text="Schaltfläche Link zu Irgendwo" link="https://collectionbuilder.github.io/" color="success" centered=true %}
  
#### Eine Warnung einbinden

- Warnungen -- > `{% raw %}{% include feature/alert.html text="dies ist eine *Warnung*, die einen Benutzer 'warnt'" color="warning" align="center" %}{% endraw %}`

{% include feature/alert.html text="Dies ist eine *Warnung*, die einen Benutzer mit zentral ausgerichtetem Text 'warnt'." color="warning" align="center" %}

#### Ein Modal einbinden

- Modals -- > `{% raw %}{% include feature/modal.html button="Dies ist ein Modal, das eine 'primäre' farbige Schaltfläche verwendet, um zum Anklicken aufzufordern" title="wenn angeklickt:" text="Ein Modal öffnet ein Feld mit weiteren Informationen" color="primary" %}{% endraw %}`

{% include feature/modal.html button="Dies ist ein Modal mit einer 'primären' farbigen Schaltfläche, die zum Klicken einlädt" title="Beim Anklicken:" text="Ein Modal öffnet ein Feld mit weiteren Informationen" color="primär" %} 
