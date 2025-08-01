Uživatelé a cílové skupiny
Jedná se o držitele platebních karet (fyzické osoby, příp. OSVČ) ze segmentu SME, kteří budou takto definováni ze strany Mastercard a rozlišení bude i dle BIN příslušné karty. Zde je třeba vést v patrnosti multiplikaci případů – tj. dle produktového nastavení limitovat počty případů vs. počet karet na osobu, případně podnikatelský subjekt.

Zprostředkovatelé / operátoři (advokáti a právníci nebo pracovníci platformy) – interně budou případy evidovány ve stávajícím systému, advokáti a právní kanceláře jsou v rámci externí spolupráce mimo tyto systémy – zde tedy půjde o následný export dat, který již bude řešen mimo tento web a není třeba uživatelských práv či přístupů.

Pojišťovna/asistenční společnost jako poskytovatel služby – bude třeba nastavit export dat z webu do interních systémů/úložišť společnosti tak, aby jednotlivé případy mohli být jednak primárně posouzeny před předáním na advokátní/právní kanceláři, popř. pak došlo k vyzvání klienta k doplnění nezbytných informací/dokumentů k události.
3. Uživatelský proces (User Journey)
3.1 Krok 1: Uvítací obrazovka
Níže je znázorněn mockup úvodní stránky:
 
Funkční prvky:
•	branding: Logo Mastercard + nápis
•	nadpis: „Potřebujete právní pomoc?“
•	podnadpis: „Pomůžeme Vám s vymáháním Vašich pohledávek a s přípravou podkladů“
•	navigace: „O nás“, „Služby“, „Kontakt“
•	CTA: Tlačítko „Nahlásit událost“
•	pozadí: Motiv soudního kladívka, Lady Justice
3.2 Krok 2: Ověření klienta dle platební karty
Níže je znázorněn mockup obrazovky pro zadání čísla karty:
 
Funkce a pravidla pole:
•	pouze číselný vstup (0–9), přesně 8 znaků
•	validace v reálném čase, zákaz zadávání písmen a speciálních znaků
•	placeholder „např. 1234 5678“
•	CTA tlačítko „Pokračovat“ aktivní po správném zadání
3.3 Krok 3: Formulář pro nahlášení události
Níže je znázorněn mockup obrazovky s formulářem pro nahlášení události:
 
Formulářová pole:
•	jméno a příjmení, Adresa, Telefon, E-mail, Popis události
•	validace polí (telefon, e-mail, minimální rozsah textu)
•	možnost nahrání příloh (PDF, DOC(X), PNG, JPG)
•	max. 5 příloh, do 10 MB každá (bude upřesněno)
•	z pohledu parametru produktu pak lze doplnit také IČO klienta (jedná se o OSVČ segment, dále IČO dlužníka – nesmí být nastaveno jako mandatorní pole, protože může jít o vymáhání duhu u fyzické osoby – ale v pozadí s nastaveným filtrem, aby se nejednalo o vymáhání proti Europ Assistance, Mastercard, či klientově bance
•	vymáhaná částka – půjde o pole, které bude mít nastaveno minimální hodnotu tak, abychom nevymáhali částky nižší, než je nastaveno v produktových parametrech – zároveň je třeba brát v potaz fakt, že jde o subjektivní vnímání klienta a výsledná částka, po právním posouzení, může/bude jiná, než udává klient
