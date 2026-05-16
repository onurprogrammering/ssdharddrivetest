Demo 1 opgave 1
Kursusnavn: Programmering
Kursusnummer: 02002 og 02003
Eksamensdato: 21. december 2025
Tilladt hjælpemidler: Alle hjælpemidler, intet internet
Eksamenens varighed: 4 timer
Vægtning: Alle opgaver har samme vægt
Antal opgaver: 10
Antal sider: 12
Contents
Eksamensinstruktioner
Opgave 1: Kaliberdiameter (Gauge Diameter)
Opgave 2: Gateafstand (Gate Distance)
Opgave 3: Parallelle modstande (Parallel Resistors)
Opgave 4: Graf-transponering (Graph Transpose)
Opgave 5: Ulige gennemsnit (Odd Means)
Opgave 6: Navigationssporing (Navigation Tracking)
Opgave 7: Sætningskompleksitet (Sentence Complexities)
Opgave 8: Cykellygte (Bike Light)
Opgave 9: Kuffert (Suitcase)
Opgave 10: Butiksstatus (Shop Status)
Eksamensinstruktioner
Eksamensmateriale
Eksamensmaterialet er en enkelt zip-fil, som du skal udpakke til en mappe på din computer. Zip-filen indeholder
eksamensopgaven som et pdf-dokument på engelsk 2025_12_exam_English.pdf og det samme dokument på dansk
2025_12_exam_Danish.pdf (dette dokument). Hver pdf indeholder alt, hvad der er nødvendigt for at løse eksamen.
Som ekstra hjælp indeholder zip-filen en mappe 2025_12_exam med følgende indhold:
Tomme Python-filer <task_name>.py , hvor <task_name> er navnet på opgaven. Der kan være færre filer end opgaver.
En Python-testfil for hver opgave, test_task_<n>_<task_name>.py , hvor <n> er opgavens nummer, og <task_name>
er navnet på opgaven.
En Python-fil test_tasks_all.py.
En mappe files , der indeholder datafiler, hvis der er nogen.
Løsning af eksamensopgaver
For at kunne løse eksamensopgaverne skal du have en computer med Python installeret. Alle opgaver kan løses ved hjælp af
en editor efter eget valg, f.eks. IDLE eller VS Code.
Vi anbefaler, at du bruger de medfølgende filer: Skriv dine løsninger i de tomme filer, og test dem ved at køre de medfølgende
test-scripts. Disse scripts kontrollerer, om din løsning fungerer korrekt for inputtet i opgavebeskrivelsen. Brug
test_tasks_all.py til at køre alle test på én gang. De medfølgende test-scripts antager, at current working directory er
2025_12_exam . Hvis du bruger VS Code, skal du derfor klikke på File →
Open Folder... og vælge mappen
2025_12_exam (som findes inde i den mappe, du har udpakket).
En løsning, der får fejl i den medfølgende test, er forkert. Hvis din løsning består den medfølgende test, er det ikke en garanti
for, at din løsning er korrekt.
Alle opgaver kan løses ved hjælp af de værktøjer, der undervises i på kurset. Løsninger, der importerer andre moduler end
math , numpy, os eller matplotlib , vil ikke blive bedømt. De udleverede test-scripts kontrollerer ikke dette, så det er dit
ansvar at sikre, at dine løsninger kun bruger de tilladte moduler.
Hvis du mener, at der er en fejl eller uklarhed i teksten, skal du bruge den mest rimelige fortolkning af teksten og løse opgaven
efter bedste evne. Hvis vi efter eksamen finder uoverensstemmelser i en eller flere opgaver, vil dette blive taget i betragtning
under bedømmelsen.
Evaluering af eksamen
Vi vil køre yderligere tests for hver opgave for at kontrollere, om dine løsninger fungerer som angivet i opgaven. Andelen af
korrekte tests er scoren for hver opgave. Den samlede score er gennemsnittet af scoren for hver opgave.
Aflevering
For at aflevere dine løsninger skal du uploade dine Python-filer med løsningerne til Digital Exam-systemet. I Digital Exam-
systemet kan filer afleveres enten som hoveddokument eller som bilag. Du kan uploade enhver af dine løsningsfiler som
hoveddokument og de resterende filer som bilag.
Indsend kun følgende filer med præcis disse navne. Alle andre filer vil blive ignoreret.
bike_light.py
odd_means.py
gate_distance.py
parallel_resistors.py
gauge_diameter.py
sentence_complexities.py
graph_transpose.py
shop_status.py
navigation_tracking.py
suitcase.py
Opgave 1: Kaliberdiameter (Gauge Diameter)
En 12-kaliber kugle fremstilles ved at tage et pund bly, dele det i tolv lige store dele og rulle hver del til en kugle. For en anden
kaliber, f.eks. 8-kaliber, anvendes samme procedure, men med otte lige store dele.
d n
Derfor opfylder diameteren af en -kaliber kugle
π
6
d3
=
V
n
,
hvor V 40 cm3
er volumenet af et pund bly, som er .
Skriv en funktion, der, givet n
, returnerer kuglens diameter i centimeter.
For eksempel for en kugle med kaliber 12:
6V
6 ⋅ 40 cm3
d3
=
=
= 6.3662 cm3
nπ
12π
,
d =
3 √6.3662 cm3 = (6.3662 cm3) 1
3 = 1.8534 cm.
Diameteren på kuglen med kaliber 12 er altså 1.8534
cm, og funktionen bør opføre sig som vist nedenfor.
>>> gauge_diameter(12)
1.8533610896304256
Filnavnet og kravene er:
gauge_diameter.py
gauge_diameter(n)
Computes the diameter of an n
-gauge ball.
Parameters:
n int The gauge.
Returns:
float The diameter in cm.