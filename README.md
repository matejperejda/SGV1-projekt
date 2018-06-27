# Space Wars

- jednoduchá 3D hra (pohľad zhora)
- úlohou hráča je zostreliť čo najväčší počet blížiacich sa asteroidov 
- asteoridy prichádzajú v určitých vlnách a intervaloch
- každou ďalšou vlnou sa zvyšuje obtiažnosť (navyšuje sa počet generovaných asteoridov)
- ovládanie: 
  * šípky/{W,A,S,D} - pohyb lode
  * spacebar - streľba

- vytvorenie hlavného menu

*Hlavné menu*
<p align="center">
  <img src="https://github.com/matejperejda/SGV1-projekt/blob/master/screenshots/01.jpg?raw=true" alt="main-menu-img"/>
</p>

*Okno 'About'*
<p align="center">
  <img src="https://github.com/matejperejda/SGV1-projekt/blob/master/screenshots/02.jpg?raw=true" alt="main-menu-about--img"/>
</p>

- pri tvorbe boli použitie oficiálne Unit assety (predpripravené 3D modely objektov a rôzne grafické a audio efekety)

*Začiatok hry, prvá vlna*
<p align="center">
  <img src="https://github.com/matejperejda/SGV1-projekt/blob/master/screenshots/03.jpg?raw=true" alt="game-start-img"/>
</p>

- implementácia 
	* zvukové efekty
	* práca s animáciami 
	* viac druhov osvetlení
	* tvorba tzv. *scrolling background* (pohybujúce sa pozadie dáva hráčovi pocit, že vesmíra loď skutočne letí vpred)
	* rozšírená práca s Collider-mi
	* využitie [Instantiate](https://docs.unity3d.com/ScriptReference/Object.Instantiate.html) - klonovanie objektov (generovanie asteoridov, striel,...)
  * využitie [StartCoroutine](https://docs.unity3d.com/ScriptReference/MonoBehaviour.StartCoroutine.html) - využitie pri tvorení páuz medzi vlnami asteoridov  
  * využitie [Quaternion](https://docs.unity3d.com/ScriptReference/Quaternion.html) - reprezentácia rotácií
  * ...
	
*Streľba*
<p align="center">
  <img src="https://github.com/matejperejda/SGV1-projekt/blob/master/screenshots/04.jpg?raw=true" alt="firing-img"/>
</p>  

*Koniec hry*
<p align="center">
  <img src="https://github.com/matejperejda/SGV1-projekt/blob/master/screenshots/05.jpg?raw=true  " alt="game-over-img"/>
</p>  
  
- **celý projekt** sa nachádza v súbore *sgv_project.unitypackage*, ktorý stačí naimportovať do Unity editora
- archív *sgv_project_build.zip* obsahuje **standalone aplikáciu** (exe súbor), ktorá spúšťa celú hru (buildované pre 64-bit Windows verziu)
- adresár *Script* obsahuje dôležité skripty, konkrétne: 
   * BackgroundScroller 
   * DestroyByContact 
   * DestroyByTime 
   * DestroyShotByBoundary 
   * GameController
   * LaserMover 
   * PlayerShipController
   * QuitMainMenuScene
   * RandomRotator
   * StartMainScene 
   * *(zvyšné skripty, ktoré adresár Script obsahuje patria k stiahnutým assetom a neboli nijak upravované)*
