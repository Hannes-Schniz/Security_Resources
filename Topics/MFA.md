---
tags:
  - notes
  - Security
---
# 2-Faktor Authentifizierung

2 Faktor Authentifizierung beschreibt den Vorgang zur Autorisierung der eigenen Identität gegenüber einem System, nicht lediglich ein Passwort, sondern ebenfalls einen zweiten Faktor zu verwenden. Ein Beispiel hierfür wäre das Abheben von Bargeld an einem Geldautomaten. Um diese Aktion durchzuführen, benötigt man eine Bankkarte mit zugehörigem Pin. 

Vorab sei zu klären, wie ein Faktor definiert ist. Hierbei ist es wichtig zu verstehen, dass ein zweites Passwort keinen zweiten Faktor darstellt und die Sicherheit des Zugangs nur geringfügig erhöht. Die drei gängigsten Faktoren sind:

- Wissen. Dieser Faktor kann durch das Setzen eines Passwortes bedient werden.

- Besitz. Dieser Faktor wird beispielsweise durch Zugangskarten oder Mobilgeräte bedient.

- Sein. Dieser Faktor kann beispielsweise durch biometrische Daten bedient werden.


Bei der 2 Faktor Authentifizierung müssen mindestens zwei dieser Faktoren bedient werden. Üblicherweise werden hier Wissen und Besitz gewählt, wie in dem vorangegangenen Beispiel aufgezeigt. 

## Arten von 2 Faktor Authentifizierung
Zu Beginn ist es wichtig, zwischen 2 Faktor- und Multi-Faktor Authentifizierung zu unterscheiden. Die Multi-Faktor Authentifizierung stellt eine übergeordnete Gruppe von Authentifizierungsarten dar. Hierbei kann eine beliebige Anzahl an Faktoren angewandt werden, wobei die 2 Faktor Authentifizierung lediglich 2 Faktoren vorsieht.

Diese Faktoren haben verschiedene Ausprägungen. Hier eine Liste der gängigsten Ausprägungen der oben genannten Faktoren:

  
| Wissen                                                     | Besitzen                                                                                               | Sein                                        |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ | ------------------------------------------- |
| Passwort<br><br>Sicherheitsfragen<br><br>Persönliche Daten | Endgeräte (2FA Apps)<br><br>Zugangskarten<br><br>Zahlungskarten<br><br>Hardware Token<br><br>Schlüssel | Biometrie<br><br>Gangart<br><br>Schreibstil |

Jede dieser Ausprägungen hat ihre technischen Vor- und Nachteile, auf welche ich an dieser Stelle nicht weiter eingehen werde. Ich beschränke mich lediglich auf die Art des Faktors und Nachteile der Gruppe. Hierbei hat der Faktor Wissen den Nachteil, dass Wissen geteilt werden kann. Eine Information ist nie garantiert privat und daher kann der Faktor durch das einfache Erlangen des Wissens umgangen werden. Der Faktor des Besitzes kann durch beispielsweise Diebstahl oder dem Kopieren des genutzten Faktors umgangen werden. Der Faktor des Seins ist am schwierigsten zu umgehen und in vielen Fällen beinahe unmöglich. Hierbei muss versucht werden, die Technik mittels gefälschter Identitäten zu täuschen.

## Vorteile von 2 Faktor Authentifizierung

Die 2 Faktor Authentifizierung hat neben dem deutlichen Gewinn an Sicherheit noch viele weitere Vorteile gegenüber der Ein-Faktor Authentifizierung. 

Doch schon der Zugewinn an Sicherheit macht 2FA in vielen Fällen unverzichtbar. Laut Statista ist die durchschnittliche Länge eines Passworts in den USA im Jahre 2021 zwischen 8 und 11 Zeichen. Laut der Website The Security Factory ist die durchschnittliche Dauer zum Cracken eines gehashten Passworts dieser Länge bei 632Gh/s und einem Character Set von Zahlen, Groß- und Kleinbuchstaben zwischen 6 Minuten und 15 Jahren. Diese Zahlen beziehen sich allerdings auf reine Brute Force Angriffe. Diese Zahlen verringern sich erheblich bei Anwendung eines Dictionary oder Credential Stuff Angriffs. Bei Verwendung eines zweiten Faktors kann sich der Angreifende, selbst wenn das Passwort erraten wurde, keinen Zugriff auf den Account oder das System verschaffen, da kein Zugriff auf den zweiten Faktor besteht.

## Nachteile von 2-Faktor Authentifizierung

2 Faktor Authentifizierung hat nur wenige Nachteile. Einer dieser Nachteile ist, dass um den besten Schutz zu erreichen, benötigt es eine 2-Faktor Authentifizierung über zwei Geräte oder Medien. Dies verlangt von dem Nutzer, dass dieser mehr als nur ein Gerät mit sich führt. Dies kann zu Problemen führen, sobald der Nutzer sich an dem System authentifizieren will, falls dieser einen der beiden Faktoren nicht bei sich trägt. Ebenso können Dritte, die sich im Besitz des zweiten Faktors befinden, einfacher, mittels Social Engineering, Zugang zu Systemen wie Online-Accounts verschaffen. Jedoch sei an dieser Stelle erwähnt, dass die Vorteile der Nutzung von 2FA die Nachteile bei weitem übersteigen.

## 2-Faktor Authentifizierung umgehen

Anders als Passworte, kann man die meisten Faktoren nicht durch einfaches Erraten umgehen. Die gängigsten Methoden, einen zweiten Faktor zu umgehen bestehen in Session Hijacking und Social Engineering. Bei einem Session Hijacking Angriff, übernimmt der Angreifende eine bereits authentifizierte Session des Systems. Hierbei hat sich der Nutzer bereits authentifiziert und bekommt einen so genannten “Session Cookie”. Dieser belegt, dass sich der Nutzer bereits an dem System autorisiert hat. Falls ein Angreifer in Besitz dieses Session Cookies kommt, beispielsweise durch die Übernahme des Browsers, in welchem dieser Cookie gespeichert ist, so kann der Angreifer alle Sicherheitsvorkehrungen umgehen. Social Engineering greift dagegen den Nutzer selbst an. So kann sich der Angreifer beispielsweise als Mitarbeiter des Services ausgeben und nach einem Verifizierungscode fragen, welcher allerdings der 2FA Code des Opfers ist. Dieser Angriff umgeht jegliche technische Sicherheitsvorkehrungen und kann lediglich durch Aufklärung und Sensibilisierung des Opfers gegen diese Art von Angriffen abgewendet werden.