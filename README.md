# Analiza Interdependenței dintre Guvernanță, Sistemul Energetic și Accesul la Electricitate în Africa (2000–2023)

## 1. Descrierea Proiectului

Proiectul investighează interdependența dintre calitatea guvernanței, dezvoltarea infrastructurii energetice și accesul la electricitate în țările africane, în intervalul 2000–2023. Problema centrală este abordată prin prisma a trei întrebări de cercetare fundamentale:

- **În ce măsură calitatea guvernanței influențează dezvoltarea capacității de energie regenerabilă?**
- **Cum sunt caracteristicile tehnice ale sistemului (capacitate, pierderi, structura producției) asociate cu nivelul accesului la electricitate?**
- **Există diferențe regionale semnificative în dinamica acestor relații între regiunile Africii?**

Obiectivele cercetării vizează cuantificarea acestor relații, analizând guvernanța ca factor structural, sistemul energetic ca mecanism intermediar și accesul la electricitate ca rezultat social.

## 2. Surse de Date și Literatură

### 2.1 Surse de Date

Pentru a răspunde întrebărilor, am integrat date din două surse majore:

- **WDI (World Development Indicators)**: Pentru variabilele socio-economice (PIB real, indici de guvernanță: Controlul Corupției, Eficiența Guvernamentală, Calitatea Reglementării, Statul de Drept)
- **EIA (Energy Information Administration)**: Pentru datele tehnice privind producția, capacitatea instalată și tipologia surselor de energie

Aceste seturi de date facilitează o analiză pe termen lung, permițând corelarea politicilor publice cu realitatea infrastructurii.

### 2.2 Literatură de Specialitate

Metodologia și interpretarea rezultatelor din acest proiect se bazează pe următoarele studii recente din literatura de specialitate:

#### Bidiasse, H., Ntah, M. N., & Kogueda, F. B. A. (2025)
**"Access to electricity in Africa: the importance of the independence of regulatory authorities"**

**Relevanță:** Acest studiu demonstrează statistic, pe baza datelor din 40 de țări (2000–2021), că autonomia instituțională reală crește rata de acces la electricitate cu aproximativ 8,1%.

**Utilizare în proiect:** Lucrarea validează utilizarea indicilor de guvernanță ca predictori relevanți pentru performanța sectorului energetic și justifică teoretic legătura cauzală dintre calitatea instituțiilor și rezultatele sociale, cum este accesul la electricitate.

#### Ndayishimiye, V., et al. (2025)
**"Power generation overcapacity in selected sub-Saharan African countries: political-economic drivers and grid infrastructure challenges"**

**Relevanță:** Autorii analizează paradoxul prin care anumite țări înregistrează surplus de capacitate de generare, dar mențin rate scăzute de acces, din cauza investițiilor disproporționate (97% în generare față de doar 0,2% în rețea).

**Utilizare în proiect:** Studiul oferă suportul teoretic pentru Modelul 2 din analiza noastră, explicând de ce capacitatea instalată singură nu garantează accesul populației și de ce starea rețelei (reprezentată în modelul nostru prin pierderi și distribuție) joacă un rol critic.

#### Sarkodie, S. A., & Adams, S. (2020)
**"Electricity access, human development index, governance and income inequality in Sub-Saharan Africa"**

**Relevanță:** Sarkodie și Adams analizează modul în care accesul la electricitate, nivelul de dezvoltare și calitatea guvernanței sunt legate în țările din Africa Subsahariană. Metodele cantitative utilizate pe datele panelului demonstrează că accesul la electricitate este pozitiv corelat cu indicatorii de dezvoltare, în timp ce inegalitățile instituționale și guvernarea inadecvată împiedică extinderea infrastructurii energetice.

**Utilizare în proiect:** Articolul subliniază că includerea variabilelor de guvernanță și dezvoltare economică (cum ar fi PIB pe locuitor) în analiza accesului la electricitate este esențială, susținând utilizarea indicatorilor WDI în proiectul actual.

#### Ren, X., Zhang, X., & Jiang, Y. (2025)
**"The coordination between urban population growth and economic development in African countries"**

**Relevanță:** Ren, Zhang și Jiang studiază relația dintre dezvoltarea economică a națiunilor africane și creșterea populației urbane, examinând modul în care urbanizarea este legată de creșterea economică și cererea de infrastructură și servicii publice.

**Utilizare în proiect:** Oferă un cadru teoretic pentru înțelegerea rolului urbanizării în dezvoltarea infrastructurii energetice, justificând includerea factorilor de control precum populația urbană și PIB pe locuitor.

#### Res4Africa Foundation (2025)
**"Access to electricity in urban and peri-urban areas in Sub-Saharan Africa"**

**Relevanță:** Raportul evidențiază diferențele semnificative de acces între tipurile de așezări și regiuni, subliniind importanța contextului instituțional și a infrastructurii prin date și studii de caz.

**Utilizare în proiect:** Oferă context aplicat și argumente empirice care susțin utilizarea analizei cantitative a variabilelor de acces, urbanizare și dezvoltare economică.

## 3. Metodologie și Pașii Proiectului

### Pasul 1: Definirea Problemei
**Responsabili:** Toată echipa

S-au stabilit obiectivele, unitatea de analiză (țări africane, împărțite în două regiuni: Africa de Nord și Africa Subsahariană) și intervalul de timp (2000-2023).

### Pasul 2: Colectarea Datelor (Data Collection)
**Responsabili:** Mihăilă Delia-Mădălina (01_eia_data_student1.ipynb) și Enache Răzvan-Andrei (02_wdi_data_student2.ipynb)

#### Colectarea datelor EIA
Pentru analiza relației dintre accesul la electricitate și dezvoltarea economică, s-au utilizat date energetice furnizate de **U.S. Energy Information Administration (EIA)**, accesate prin intermediul API-ului oficial EIA v2 International Data. Această sursă oferă serii temporale consistente și comparabile la nivel de țară privind producția și consumul de electricitate.

A fost selectat un set de **14 produse energetice relevante**, incluzând consumul și producția de electricitate, precum și alte surse de generare (hidro, nuclear, regenerabile). Datele au fost filtrate geografic utilizând coduri ISO3 pentru țările africane.

#### Colectarea datelor WDI
La nivelul **World Development Indicators (WDI)** a fost elaborat un cod pentru colectarea informațiilor aferente fiecărei națiuni din Africa, pentru perioada 2000–2023. Selecția țărilor africane a fost realizată prin filtrarea statelor pe baza clasificării regionale furnizate de WDI.

**Indicatorii principali:**
- Accesul populației la electricitate (EG.ELC.ACCS.ZS)
- Produsul intern brut pe cap de locuitor (NY.GDP.PCAP.KD)
- Ponderea populației urbane (SP.URB.TOTL.IN.ZS)

**Indicatori instituționali și sociali:**
- Capacitatea de reglementare a guvernului (RQ.EST)
- Statul de drept (RL.EST)
- Controlul corupției (CC.EST)
- Eficiența guvernamentală (GE.EST)
- Coeficientul Gini (SI.POV.GINI)

Perioada de analiză a fost limitată la intervalul **2000–2023**, întrucât pentru anii cei mai recenți baza WDI prezintă un grad ridicat de date lipsă.

### Pasul 3: Curățare și Integrare (Cleaning & Merging)
**Responsabil:** Năstase Andrei Valentin (03_cleaning_aggregation_student3.ipynb)

Pentru etapa de curățare și pregătire a datelor, cele două surse au fost tratate separat:

**Curățarea datelor EIA:**
- Analiza coloanelor disponibile, valorilor lipsă per coloană și per țară
- Eliminarea coloanelor redundante (dataFlagid, productID etc.)
- Transformarea în format CSV și încărcarea în NEON

**Curățarea datelor WDI:**
- Eliminarea anului 2001 (98% date lipsă)
- Eliminarea indicatorului Gini_coefficient (84% date lipsă)
- Transformarea în format CSV și încărcarea în NEON

**Integrarea datelor:**
Al treilea pas a constat în unirea celor două tabele și pivotarea tabelului final. Coloanele au fost redenumite și ordonate similar în ambele tabele, apoi concatenate. Fișierul rezultat a fost pivotat și încărcat în NEON pentru analiza exploratorie.

### Pasul 4: Analiza Exploratorie (EDA)
**Responsabil:** Ciucea Iarina (04_descriptive_statistics_student4.ipynb)

S-a realizat o analiză vizuală și descriptivă a setului de date integrat pentru a înțelege distribuțiile variabilelor și a identifica tendințele preliminare. Un element cheie a fost extinderea tabelului prin adăugarea unei clasificări geografice explicite: **Northern Africa** și **Sub-Saharan Africa**.

**Activități principale:**

- **Analiza Univariată:** Histograme și statistici descriptive pentru distribuția variabilelor cheie. S-a constatat o asimetrie puternică a datelor economice, justificând necesitatea logaritmării PIB-ului.

- **Analiza Bivariată:** Grafice scatter plot care au evidențiat o legătură pozitivă între PIB per capita și capacitatea regenerabilă.

- **Comparații Regionale:** Utilizarea boxplots pentru diferențierea profilului energetic:
  - **Northern Africa:** PIB ridicat și acces la electricitate aproape universal (>90%), dar dependentă de fosili
  - **Sub-Saharan Africa:** Variabilitate extremă și rate scăzute de acces, dar cu potențial mare neexploatat

**Concluzie EDA:** Analiza a confirmat disparități structurale majore între cele două regiuni, validând decizia de a utiliza împărțirea geografică ca factor de control în modelele statistice ulterioare.

### Pasul 5: Feature Engineering și Analiză Statistică
**Responsabil:** Ciutu Carmen-Alexandra (05_feature_engineering_analysis_CiutuCarmen.ipynb)

#### A. Feature Engineering (Transformarea Datelor)

- **Index de guvernanță (governance_index):** Creat prin media aritmetică a celor 4 indicatori WDI (Control of Corruption, Rule of Law, Regulatory Quality, Gov Effectiveness) pentru a reduce multicoliniaritatea

- **Indicatori relativi:** Calcularea variabilelor per capita (Capacitate, Generare, CO2) și a ponderilor (renewables_share, coal_share) pentru a permite comparația între țări de dimensiuni diferite

- **Transformări logaritmice:** Aplicarea log() asupra PIB-ului (log_gdp_per_capita) pentru a normaliza distribuția și a liniariza relația cu consumul de energie

#### B. Modele Statistice și Rezultate

**Model 1 (Determinanții regenerabilelor):**
- Guvernanța are un impact marginal (p-value = 0.09)
- Coeficientul PIB-ului este negativ, sugerând că țările mai bogate din Africa tind să se bazeze istoric pe combustibili fosili, nu pe regenerabile

**Model 2 (Accesul la Electricitate):**
- Model performant (R² ≈ 0.75)
- Variabila electricity_distribution_losses are un coeficient pozitiv semnificativ, indicând că extinderea rețelei (chiar dacă este ineficientă și are pierderi tehnice) este principalul motor al accesului, alături de PIB
- Dezvoltarea economică este motor principal
- Politici optime combină stimulare creștere + investiții infrastructură + îmbunătățiri instituționale

**Analiză Regională (ANOVA):**
- Diferență structurală majoră între Africa de Nord și Africa Subsahariană în privința accesului la electricitate (medie 87% vs 58%, p < 0.01)
- Nu există diferențe semnificative statistic în ceea ce privește calitatea guvernanței sau cota de energie regenerabilă între cele două regiuni

## 4. Concluzii

**Dezvoltarea economică dictează accesul, dar nu și "înverzirea":** PIB-ul este cel mai puternic predictor pentru accesul la electricitate, dar corelează negativ cu cota de regenerabile, indicând că țările africane au urmat până acum calea convențională de dezvoltare (bazată pe fosili).

**Paradoxul guvernanței:** Calitatea instituțiilor (birocrația, corupția) nu pare să fie blocajul principal pentru energia regenerabilă. Factorii tehnici și resursele naturale sunt mai importanți.

**Cele două Africi:** Există o diferență clară de dezvoltare între Africa de Nord și cea subsahariană doar la nivel de acces (infrastructură de bază), nu și la nivel de politici (guvernanță) sau intenții verzi, ceea ce sugerează că Sudul are nevoie de investiții masive în infrastructură fizică pentru a recupera decalajul.

## 5. Dificultăți și Limitări

În derularea proiectului, au fost identificate o serie de limitări care influențează interpretarea rezultatelor:

**Lacune temporale:** Un obstacol major a fost lipsa completă a datelor pentru anii 2001 și 2024 în sursele utilizate. Din cauza acestor lacune, am fost nevoiți să restrângem intervalul temporal al analizei, oprindu-ne la datele disponibile până la finalul anului 2023 și tratând cu precauție discontinuitățile de la începutul perioadei.

**Agregarea indicatorilor de guvernanță:** Din punct de vedere statistic, utilizarea indexului agregat de guvernanță a reprezentat o decizie metodologică deliberată și necesară. Deși această abordare comprimă dimensiuni distincte (precum corupția, statul de drept sau calitatea reglementării), ea a fost esențială pentru a evita multicoliniaritatea severă existentă între acești indicatori, care tind să evolueze identic. O analiză disociată pe fiecare dimensiune ar fi complicat inutil modelele, crescând redundanța statistică fără a oferi o claritate suplimentară asupra tendințelor macro. Astfel, indexul constituie soluția optimă pentru a surprinde semnalul general al calității instituționale asupra sectorului energetic, menținând analiza într-un cadru clar și interpretabil.

