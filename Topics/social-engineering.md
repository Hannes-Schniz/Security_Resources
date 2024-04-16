# 👁Überblick

Social Engineering wird von dem Bundesamt für Sicherheit in der Informationstechnik als "Ausnutzen des Faktor Menschen um kriminelle Absichten zu verwirklichen" definiert. Dementsprechend stellt ein Social engineering Angriff meist einen weniger technischen Angriff dar.
Bei einem Social Engineering Angriff werden beispielsweise zwischenmenschliche Beziehungen vorgetäuscht oder ausgenutzt. Das Opfer handelt meist in der Überzeugung etwas gutes oder richtiges zu tun, indem der Angreifer vorgibt ein Problem zu haben oder ein Problem festgestellt zu haben.
Weitere Indikatoren eines Social Engineering Versuchs sind das Ausüben von Druck auf das Opfer. Dabei wird ein auf besondere Dringlichkeit Wert gelegt um dem Opfer keine Zeit zur Reflexion zu geben und damit das Sicherheitsverständnis des Opfers zu umgehen. Des weiterem wird oft eine vermeintliche autoritäre Instanz geschaffen um die Angst von Menschen eine Anfrage einer vermeintlich höher gestellten Person abzulehnen auszunutzen.
Angst ist auch bei anderen Techniken ein entscheidender Faktor. Das Ausnutzen von Druck jeglicher Art ist ein sehr wichtiges Mittel, da Menschen, welche unter Druck oder Stress agieren oftmals anfällig sind Fehler zu begehen und Sicherheitsvorkehrungen zu missachten.
Allerdings wird in einigen Fällen auch das exakte Gegenteil, die Langeweile und Routine des Opfers ausgenutzt. Hierbei wird eine alltägliche Situation erschaffen bei der darauf gehofft wird, dass das Opfer ohne die Situation zu prüfen die Aktion ausführt, da diese alltäglich erscheint.
Diese Vorgehen können beliebig verknüpft werden um verschiedenste Angriffsszenarien zu erzeugen. Beispielsweise kann eine banal wirkende Anfrage kurz vor der Mittagspause gestellt werden in welcher auf Dringlichkeit gepocht wird, wodurch das Opfer geneigt ist diese schnell ohne eingehende Prüfung zu bearbeiten.
Eine besonders im Banken und Investment Sektor beliebte Taktik ist das Versprechen von hohen Gewinnen um die Gier des Opfers an zu sprechen.
Diese Taktiken können auf das Opfer angepasst sein um die Wahrscheinlichkeit eines erfolgreichen Social Engineering Angriffes zu erhöhen.

# ⚙Ablauf

1. Informationsbeschaffung über das Opfer
   Hierbei werden Informationen beispielsweise durch OSINT(Open Source Intelligence) Recherchen oder durch einfache Phishing versuche oder ähnlichen Methoden gesammelt um aufgrund dieser Daten ein Profil des Opfers zu erstellen.
2. Aufbau von Kontakten / Fälschung von Identitäten
   In diesem Schritt wird das vorab erarbeitete Opferprofil genutzt um Kontakt mit relevanten Personen aufzubauen, ggf. bereits Vertrauensverhältnisse auf zu bauen oder eine falsche Identität zu erschaffen mittels Social Media o.ä.
3. Informationen über das Ziel Erarbeiten
   Mittels dem bereits aufgebauten Kontakt werden nun die benötigten Informationen erarbeitet.
4. Exfiltrierung
   Sobald die nötigen Informationen erarbeitet wurden muss sich der Angreifer nun wieder aus der Situation begeben. Hierbei ist es wichtig, dass der Angriff nicht bemerkt wird um die Integrität der Information zu wahren. Auch ist hilfreich den Kontakt aufrecht zu erhalten, falls weitere Informationen o.ä. benötigt werden.
5. Informationen verarbeiten
   Die gesammelten Informationen müssen nun in einen Zusammenhang gebracht werden. Hier können auch banal erscheinende Informationen zu dem Gesamtbild beitragen. Meist kann die Information nicht direkt sondern nur Teile erarbeitet werden in diesem Schritt werden die Bruchteile der Information zusammen gefügt.

# 🛠Techniken

## Phishing

Phishing ist die am weitesten verbreitete Variante des Social Engineerings. "Phishing ist eine Form des Trickbetrugs mit Methoden des Social Engineerings.[…]" Hierbei handelt es sich um den Versuch dem Opfer sensible Daten wie Login Daten oder ähnliches durch meist automatisch generierte weit verstreute Nachrichten zu entlocken. Hier werden oft Techniken wie das Versenden von Emails mit Link zu einer vermeintlich echt wirkenden Login Maske eingesetzt.

Phishing hat noch einige Spezialformen:

### Voice Phishing (vishing)

Dabei werden Phishinganfragen telefonisch gestellt. Diese Technik wurde stark vor der Einführung des Internets eingesetzt, wurde durch die Entstehung von Deepfakes und Ai Imitationen von Stimmen gefährlicher.

### SMS Phishing (smishing)

Bei dieser Phishing Technik werden die Phishing Anfragen über SMS oder andere Messenger Dienste gestellt.

### Search Engine Phishing

Diese Phishing Technik nutzt Suchmaschinen aus. Hierbei werden Phishing Seiten in dem Ranking der Suchmaschine besonders erhöht um möglichst viele potentielle Opfer auf die Seite zu locken.

### Angler Phishing

Bei einem Angler Phishing Angriff wird die Tatsache, dass viele Unternehmen beispielsweise Support Anfragen über Soziale Netzwerke annehmen ausgenutzt. Es werden gefälschte Social Media Accounts erstellt um diese Anfragen an zu nehmen und somit den Kunden sensible Daten zu entlocken.

## Baiting

Baiting ist eine Technik bei der das Opfer durch ein gutes oder gar kostenloses Angebot zu einer Tat verleitet werden soll. Beispielsweise durch das Angebot kostenloser USB-Sticks.

## Tailgating (Piggybacking)

Tailgating beschreibt das direkte Folgen einer anderen Person in einen gesicherten Bereiches oder auch sich Zugang durch unverschlossene Türen oder zu nicht gesperrten Geräten zu verschaffen. Hier wird oft die Hilfsbereitschaft der anderen (das Aufhalten von Türen) ausgenutzt. Um diese Hilfsbereitschaft oder das Schuldgefühl die Hilfe verweigert zu haben zu bestärken versetzt der Täter sich oft in eine fiktiv hilfsbedürftige Lage.

## Pretexting

Hierbei wird ein fiktives Problem geschaffen für welches sich der Angreifer als der richtige Ansprechpartner um dieses Problem zu beheben präsentiert.

## Quit pro quo

Der Angreifer schlägt dem Opfer ein Tauschgeschäft vor, bei dem der Angreifer die Informationen im tausch einer anderen Leistung erhält.

## Scareware

Scareware bezeichnet Software, welche dazu gedacht ist, das Opfer ein zu schüchtern oder Angst zu erzeugen. So wird beispielsweise mit fiktiven Anschuldigungen Druck auf das Opfer erzeugt und im Nachgang die Herausgabe von Informationen oder Geld gefordert.

## Watering Hole Attack

Bei einem Watering Hole Angriff wird Schadsoftware in eine viel besuchte Website eingeschleust um sich Zugang zu beispielsweise Nutzerbezogene Daten wie Login Daten zu verschaffen.

# 📦Ressourcen

# 🏦Relevanz

Percentage of organizations worldwide that experienced cyber attacks
https://www.statista.com/statistics/1376249/cyber-attack-global-firms-by-type/

Number of unique phishing sites detected worldwide
https://www.statista.com/statistics/266155/number-of-phishing-domain-names-worldwide/

# 🔗 Quellen

## Überblick

- https://www.bsi.bund.de/DE/Themen/Verbraucherinnen-und-Verbraucher/Cyber-Sicherheitslage/Methoden-der-Cyber-Kriminalitaet/Social-Engineering/social-engineering_node.html - https://christian-grafe.de/wiki/Social%20Engineering%20-%20Christian%20Grafe.pdf - https://www.ibm.com/topics/social-engineering

## Techniken

- https://attack.mitre.org/techniques/T1598/
- https://attack.mitre.org/techniques/T1566/
- https://attack.mitre.org/techniques/T1589/

## Die Entwicklung von Social Engineering

- https://www.social-engineer.org/social-engineering/artificial-intelligence-the-evolution-of-social-engineering/
- https://www.terranovasecurity.com/blog/what-has-changed-in-social-engineering

## Beispiele

- https://www.social-engineer.org/framework/general-discussion/real-world-examples/
- https://www.mimecast.com/de/blog/5-common-examples-of-social-engineering/

## Zahlen, Daten, Fakten

- https://www.splunk.com/en_us/blog/learn/social-engineering-attacks.html
- https://secureframe.com/blog/social-engineering-statistics
- https://www.varonis.com/blog/cybersecurity-statistics
- https://www.researchgate.net/publication/355754456_Impact_of_Social_Engineering_Attacks_A_Literature_Review
