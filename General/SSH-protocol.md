### Protokół SSH

SSH - Secure Shell

Protokół SSH zapewnia nawiązanie bezpiecznego połączenia ze zdalnym komputerem. Jest to zestaw zasad, według których odbywa się komunikacja.

Dane przesyłane w ten sposób są szyfrowane, w przeciwieństwie do protokołów typu: FTP czy Telnet.

Protokół SSH umożliwia przeprowadzenie procesu uwierzytelnienia za pomocą zestawu kluczy prywatnych i publicznych (**Private and Public Key**). Klucze są trudniejsze do złamania niż zwykłe hasło.

Generowanie kluczy:

`ssh-keygen -t rsa-C "pb.markowska@gmail.com"`

Domyślnie zestaw kluczy zostanie zapisany w katalogu domowym w pliku. 
