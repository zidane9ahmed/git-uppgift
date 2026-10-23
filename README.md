\# Git-uppgift



\## 1. Versionshantering och vanliga filer



\### G

När jag sparar en fil med Ctrl+S sparas bara filen som den ser ut just nu, och den gamla versionen försvinner. Med Git sparar jag en version av projektet med ett meddelande om vad jag har ändrat, och de gamla versionerna finns kvar. Då kan jag gå tillbaka om något blir fel och se vad som ändrades och när.



\### VG

Den första committen är en bild av hur filen såg ut just då jag gjorde den, och Git ändrar inte den bilden efteråt. När jag ändrade filen senare och gjorde en ny commit blev det en ny bild bredvid den gamla. Därför visar den första committen fortfarande TODO, fast filen ser annorlunda ut nu.



\## 2. Arbetsyta, staging och commits



\### G

`git status` visar vad som har hänt i projektet just nu, alltså vilka filer jag har ändrat och vilka som är redo för nästa commit. `git add` väljer vilka ändringar som ska vara med i nästa version, ungefär som att lägga dem i en korg först. `git commit` tar det som ligger i korgen och sparar det som en ny version med ett meddelande om vad jag gjort. Om jag glömmer `git add` kommer ändringen inte med i committen, även om jag har sparat filen med Ctrl+S.



\### VG

Arbetsytan är mappen där jag ändrar filerna, staging är en sorts väntelista för det som ska med nästa gång, och commit är när det sparas i historiken. När jag ändrar en fil ligger ändringen bara i arbetsytan, och Git sparar den inte förrän jag lagt den i staging med `git add`. Därför säger Git `no changes added to commit`: filen är ändrad, men det finns inget i staging att spara. När jag kör `git add` kommer ändringen till staging, och sedan kan `git commit` spara den som en ny version.



\## 3. Repot på datorn och repot på GitHub



\### G

Repot på min dator är det lokala, där jag gör ändringar och commits. Repot på GitHub är en kopia på internet som ligger på en server. När jag gör en commit sparas den bara på min dator och kommer inte till GitHub av sig själv. `git push` skickar mina commits från datorn till GitHub, så att de finns där också och andra kan se dem.



\### VG

`git push` skickar bara commits, inte ändringar i filer. När jag har ändrat filen men inte gjort `git add` och `git commit` finns det ingen ny commit på min dator som GitHub saknar. Git jämför commits och ser att allt som är sparat som commit redan ligger på GitHub, och därför säger den `Everything up-to-date`. Ändringen ligger bara i arbetsytan och är inte sparad som en version, så det finns inget att skicka.

