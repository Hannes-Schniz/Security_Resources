---
tags:
  - notes
  - Security
  - passwords
---
# Passworte

Passworte werden seit jeher zur Sicherung jeglicher Systeme verwendet. Bereits vor der Erfindung des Internets oder gar des Computers wurden Passworte zur Zugangsbeschränkung zu gesicherten Bereichen oder Informationen verwendet. 

Das erste digitale Passwort wurde im Jahre 1961 von einem Professor des MIT namens Fernando Corbato entwickelt. Hierbei sollten Zugriffe auf ein gemeinsames System über die Verwendung nutzerspezifischer Passworte gesichert und unterschieden werden. 

Heute werden Passworte zur Sicherung jeglicher online und offline Accounts und Systeme eingesetzt. Sie stellen den einfachsten Weg dar, den Zugriff auf den betroffenen Account zu beschränken. Allerdings ist es mit dem Setzen eines Passwortes oft nicht getan. Brute-Force Angriffe, Dictionary Attacks oder Passwort Cracking können dennoch dazu führen, dass sich Außenstehende Zugriff zu diesen vermeintlich gesicherten Bereichen verschaffen. Daher ist es wichtig, einige Regeln einzuhalten, welche im folgenden erläutert werden.

## Passworte und Passphrasen

Passworte sind den meisten ein Begriff, Passworte wie "Sommer2023" werden häufig zur Sicherung von privaten oder sogar geschäftlichen Accounts verwendet. Ein Passwort ist laut verschiedener Onlinequellen als “Ein Passwort ist eine Zeichenfolge, die zur Zugangs- oder Zugriffskontrolle eingesetzt wird" definiert. Im Allgemeinen wird ein Passwort als üblicherweise 4-10 Zeichen langer Schlüssel verstanden. Hierbei ist es unerheblich, ob die Zeichen zusammenhängen und welchen Inhalt dieser Schlüssel widerspiegelt. 

Passphrasen sind üblicherweise länger, hierbei handelt es sich um eine Aneinanderreihung von Worten, die das Passwort bilden. Üblicherweise sind diese Passphrasen mindestens 14 Zeichen lang und bieten alleine durch ihre Länge besseren Schutz gegen Brute Force Angriffe.

## Passwortrichtlinien

Viele Unternehmen oder Dienste geben verschiedene Passwortrichtlinien als Minimalanforderung vor. Dies könnte zum Beispiel die Länge des Passwortes sein, die Nutzung von Sonderzeichen oder Groß-/Kleinschreibung.  Dies sind allerdings nur Minimalanforderungen an die Passwortsicherheit. Das Passwort “Admin!” erfüllt alle diese Kriterien, ist allerdings kein sicheres Passwort. Um ein tatsächlich sicheres Passwort zu generieren, müssen einige weitere Richtlinien eingehalten werden. Dennoch ist zu beachten, dass es nicht genügt, nur eine Teilmenge der genannten Richtlinien zu erfüllen. Um ein sicheres Passwort zu erzeugen, sollten alle Richtlinien zumindest zu Teilen beachtet werden. Ein langes Passwort, welches nur aus einem Buchstaben besteht, ist ebenso sicher wie ein Passwort, welches aus 3 randomisierten Zeichen besteht.

### Passwortlänge

Hierbei gilt es nicht auf eine Mindestanforderung zu setzen, sondern die Fragestellung umzukehren. Um ein möglichst sicheres Passwort zu erzeugen, sollte die maximal mögliche Passwortlänge genutzt werden. Wie später diskutiert ist hierbei die Verwendung einer Verwaltungssoftware zu empfehlen. Für Passworte, welche nicht durch eine Verwaltungssoftware verwaltet werden sollen, sind 10-16 Zeichen ein guter Richtwert.

### Groß-/Kleinbuchstaben, Sonderzeichen und Zahlen

Um ein sicheres Passwort zu generieren, sollte das gesamte Zeichen-Spektrum abgedeckt werden. Dieses Spektrum besteht meist aus Groß-/Kleinbuchstaben sowie Sonderzeichen, mit Ausnahme einzelner Zeichen und Zahlen.

### Keine Worte verwenden

Eine wichtige Richtlinie bezieht sich auf die Verwendung von in Wörterbüchern vorkommenden Worte. Diese sind mittels eines sogenannten “Dictionary Attacks" angreifbar. Hierbei versucht ein Angreifer mittels des Kombinierens von Worten einer Wortsammlung ein Passwort zu erraten. Um sich vor dieser Art von Angriffen zu schützen, sollten Worte aus Wörterbüchern vermieden werden.

### Keine persönlichen Daten

Oft werden persönliche Daten wie das Geburtsdatum, der Geburtsort, der Nachname, etc. verwendet. Dies sind potentiell öffentlich bekannte oder einsehbare Informationen. Ein Passwort ist per definition geheim. Mittels so genannten Phishing Angriffen oder einer “OSINT”(Open Source Intelligence) Recherche können viele dieser vermeintlich privaten Informationen gefunden werden und sind daher nicht als geheim anzusehen. Diese können wiederum dazu verwendet werden, das gewählte Passwort zu erraten.

  

## Gefahren bei Wiederverwendung von Passworten

Um seine Nutzerprofile zu sichern, sollte man jedes einzelne mittels eines Passworts sichern. Da jeder Internetnutzer eine Vielzahl von Benutzerkonten besitzt, liegt der Gedanke nahe, sich ein sicheres Passwort zu generieren und dieses zur Sicherung aller Konten zu verwenden. Dieses Vorgehen mag auf den ersten Blick komfortabel erscheinen, so ist jedes Konto mit einem starken Passwort geschützt. Allerdings macht man sich durch das Wiederverwenden des Passworts durch so genannte “Credential Stuffing” oder “Password Spraying"  angreifbar. So kann das Passwort in einem Datenleck eines der angemeldeten Services an die Öffentlichkeit gelangen. Daher sollte für jedes Konto ein eigens erstelltes Passwort verwendet werden. Diese sollten möglichst wenig miteinander gemein haben. 

## Passwortverwaltung

Zur Verwaltung der Passworte sollte möglichst eine Verwaltungssoftware verwendet werden. Diese Software nimmt dem Nutzer nicht nur die Speicherung, sondern auch die Erstellung der Passworte ab. Dies hat den Vorteil, dass das Programm kein Muster bei der Erstellung des Passwortes anwendet, um sich das Passwort merken zu können. So sind die durch das Programm erstellte Passworte immer beliebig und nahezu unmöglich zu erraten. Ebenfalls weiß der Nutzer eines solchen Programms oftmals die durch das Programm gesetzte Passwort selbst nicht. Auf den ersten Blick wirkt dies schlecht, jeder hat zuvor ein Passwort vergessen, was einen erheblichen Mehraufwand verursacht hat. Allerdings ist die Unwissenheit über das gesetzte Passwort in diesem Fall ein Vorteil der Verwaltungssoftware. Durch die Unkenntnis kann es nicht passieren, dass das Passwort versehentlich in falschen Anmelden Feldern eingegeben werden. Das Programm speichert sich das Passwort relativ zur Adresse der Internetseite und fügt das Passwort in die korrekten Textfelder ein. Dies ist ein Schutz gegen gefälschte Anmeldeseiten, welche zur Erschleichung von Login Daten erstellt wurden, da das automatische Ausfüllen der Textfelder dort nicht ausgeführt wird.

## Angriffe auf Passworte

In den vorangegangenen Kapiteln habe ich schon einige Angriffstaktiken auf Passworte genannt, hier will ich noch einmal auf einige etwas genauer eingehen und die Technik dahinter beleuchten.

  

### Brute Force Attacke

Die Brute Force Attacke ist die rudimentärste Art, sich Zugang zu dem Passwort eines Nutzers zu verschaffen. Bei einem Brute Force Angriff wird versucht, durch einfaches Raten der möglichen Kombinationen das Passwort in Erfahrung zu bringen. So werden in Brute Force Tools wie beispielsweise Hydra die Parameter des Passworts festgelegt und das Tool erzeugt alle möglichen Passworte, welche zu diesen Parametern passen. Dieses Vorgehen ist sehr zeitaufwändig. So können Brute Force Angriffe Stunden, Tage oder sogar Jahre dauern. Daher ist diese Technik, wenn auch einfach, nicht universell anwendbar. Man kann sich bereits mit der Wahl eines ausreichend langen Passworts gegen diese Angriffsart schützen, da sich die möglichen Passwortkombinationen exponentiell vermehren.

Eine besondere Art der Brute Force Attacke sind der Dictionary Angriff, dieser verwendet ein so genanntes „Dictionary“, eine Liste aus beliebigen Worten und versucht diese zu kombinieren und unter Umständen leicht abzuändern. Diese Art des Angriffes zielt darauf ab, Passworte, welche aus der einfachen Kombination von Worten oder bekannten Zeichenketten bestehen, schneller zu erraten. Ein Dictionary muss in diesem Fall nicht aus den Worten einer Sprache bestehen, sondern kann beliebige Zeichen und Zeichenketten beinhalten. Eine weitere Eigenart der Brute Force Attacke stellt der Password Spraying Angriff dar. Diese Art des Angriffes zielt darauf ab, schwache Passworte schnell zu erraten. Hierbei wird ähnlich zum Dictionary Angriff eine Liste an Zeichenketten verwendet. In diesem Fall enthält diese Liste allerdings Passworte. Diese Passworte werden breit gestreut und es wird versucht, sich mithilfe diesen bei verschiedenen Nutzerkonten anzumelden.

  

### Phishing

Eine sehr weit verbreitete Methode Passworte anzugreifen, ist der Phishing-Angriff. Hierbei wird nicht das Passwort direkt als Ziel des Angriffs gewählt, sondern der Mensch, der das Passwort vergeben hat. Ein Phishing-Angriff ist sehr vielseitig. Das Opfer wird beispielsweise durch das Vortäuschen einer falschen Identität dazu verleitet, private Daten sowie Login-Daten, Adressdaten oder Antworten auf Sicherheitsfragen preiszugeben. Phishing ist ein sehr gefährlicher Angriff, besonders die Eigenart namens „Spear phishing“, bei der der Phishing Versuch auf das Opfer speziell zugeschnitten ist.

Die Schwierigkeit dieses Angriffs besteht darin, dass durch das Wechseln des Angriffsziels auf die Person die Stärke des Passworts keine Rolle spielt. Dieser Angriff kann allerdings ebenfalls durch die Verwendung einer Passwortverwaltung abgewehrt werden. So kann das fehlende automatische Ausfüllen der Login-Maske beispielsweise ein klarer Warnhinweis sein. Auch die wenigen Sekunden, die es benötigt, das Passwort nachzuschlagen, bevor man es einer fremden Person nennt oder in einer fremden Anmeldemaske einzugeben, kann zur Reflexion dienen und bei dem Opfer zur Vermeidung des Phishings führen.