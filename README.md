⚠️ Dieses Repository wird nicht weiter gepflegt, da Adobe das Projekt PhoneGap zum 01.10.2020 abgekündigt hat, siehe https://blog.phonegap.com/update-for-customers-using-phonegap-and-phonegap-build-cc701c77502c.

# Anleitung
1. map.apps App über 'Export für native App' exportieren
2. Inhalte des heruntergeladenen .zip in den `www` Ordner entpacken
3. Ordner `www` und `config.xml` zippen
4. in PhoneGap Build hochladen und bauen

# Mögliche Fehlerquellen

## Unterstützte map.apps Version
Vorgesehen ist die Nutzung dieses Rahmens für map.apps Apps ab Version **4.3**

Bei Verwendung von map.apps < 4.2.2 ist es für Android-Builds noch notwendig, folgende Experten-Einstellungen bei "weitere Module in die Layer-Datei aufnehmen" anzugeben:
    	`dojo/_base/browser,dojo/_base/unload,dojo/_base/NodeList` .

## Entwicklermodus

Für Android und Windows Apps ist es notwendig, dass sich das Zielgerät im Entwicklermodus befindet oder es erlaubt wird, Apps aus unbekannten Quellen und unsignierte Apps / Apps ohne Zertifikat zu installieren.

## Apple Account
Für iOS ist es notwendig, einen Apple Entwickleraccount zu besitzen

https://developer.apple.com/programs/ 

http://docs.phonegap.com/phonegap-build/signing/ios/ 
## Importieren des Anwendungszertifikats bei UWP-Apps
Dieser Schritt ist einmalig notwendig, wenn Windows Apps ohne eigenes Zertifikat erstellt werden.
Quelle: 

https://msdn.microsoft.com/en-us/library/windows/desktop/jj835836(v=vs.85).aspx

```
To manually add the certificate to the local computer certificate trust

* In File Explorer, right-click on the app package, and in the pop-up context menu select Properties.
* In the Properties dialog, select the Digital Signatures tab.
* In the Signature list, select the signature and then click the Details button.
* In the Digital Signature Details dialog, click the View Certificate button.
* In the Certificate dialog, click the Install Certificate… button.
* In the Certificate Import Wizard, select Local Machine and then click Next. You will need to grant administrator privileges to continue.
* Select Place all certificates in the following store and browse to the Trusted People store.
* Click Next, then click Finish to complete the wizard.
```
