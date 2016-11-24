<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

  - [Welcome {{user?.name}}](#welcome-username)
  - [FETCH PROMISE OBSERAVABLE RXJS](#fetch-promise-obseravable-rxjs)
  - [TYPESCRIPT](#typescript)
  - [ANGULAR2 CLI](#angular2-cli)
  - [NATIVESCRIPT :](#nativescript-)
  - [IONIC2 https://apps.ionic.io/apps](#ionic2-httpsappsionicioapps)
  - [syntax](#syntax)
- [pour la déclaration de variable](#pour-la-d%C3%A9claration-de-variable)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

intellij racourci : https://github.com/MrZaYaC/ng2-webstorm-snippets 

chrome : https://hackernoon.com/twelve-fancy-chrome-devtools-tips-dc1e39d10d9d#.imf6priwg 
chrome : https://medium.freecodecamp.com/10-tips-to-maximize-your-javascript-debugging-experience-b69a75859329#.o1mbuv4hn 
CHROME CORS PLUGIN OU http://crossorigin.me/ : Allow-Control-Allow-Origin: * https://chrome.google.com/webstore/detail/allow-control-allow-origi/nlfbmbojpeacfghkpbjhddihlkkiljbi 
CHROME POSTMAN PLUGIN 

SUBLIMETEXT : https://github.com/Microsoft/TypeScript-Sublime-Plugin 
ATOM :  
shortcut : https://github.com/nwinkler/atom-keyboard-shortcuts 
utility : http://stackoverflow.com/questions/32790311/how-to-structure-utility-class 
ionic2 i18n : http://www.gajotres.net/ionic-2-internationalize-and-localize-your-app-with-angular-2/ 
ng2 img : https://github.com/VadimDez/ng2-img-fallback 
loader : https://ionicframework.com/docs/v2/api/components/loading/LoadingController/ 
 
HTTP POST PARAMS : 
https://forum.ionicframework.com/t/http-post-not-sending-data/47452/6 
http://michael.laffargue.fr/blog/2016/04/17/angularjs2-send-http-post-request-with-parameters-to-php/ 
https://auth0.com/blog/angular-2-series-part-3-using-http/ 
https://www.barbarianmeetscoding.com/blog/2016/04/02/getting-started-with-angular-2-step-by-step-6-consuming-real-data-with-http/ 
 
## FETCH PROMISE OBSERAVABLE RXJS 
http://output.jsbin.com/juwiva/29 
https://angular.io/docs/ts/latest/cookbook/component-communication.html#!#bidirectional-service 
 
 
## TYPESCRIPT 
 
npm install -g typescript 
tsc --init --target es5 --sourceMap --experimentalDecorators --emitDecoratorMetadata 
tsc --watch 
npm init 
 

 
## ANGULAR2 CLI 
ng generate component pony sidebar article article_list 
ng generate class article 
ng generate service article 
ng serve 
ng build --prod	 
ng github-pages:deploy 
git subtree push --prefix dist/ origin gh-pages 
 
## NATIVESCRIPT : 
set ANDROID_HOME=C:\Android\sdk 
set PATH=%PATH%;%ANDROID_HOME%\tools;%ANDROID_HOME%\platform-tools 
 
http://docs.nativescript.org/angular/start/quick-setup 
https://docs.nativescript.org/start/ns-setup-win 
http://docs.nativescript.org/angular/tutorial/ng-chapter-1 
http://docs.nativescript.org/angular/tutorial/ng-chapter-2 
https://docs.nativescript.org/angular/code-samples/overview.html (component) 
tns run android 
tns livesync android --watch 
 
native + webapp : 
https://github.com/Appverse/PANG-Polymorphic-ANGular-seed 
http://developer.telerik.com/featured/building-angular-2-web-native-apps-single-codebase/ 

 

## IONIC2 https://apps.ionic.io/apps 
 
http://ionicframework.com/docs/v2/getting-started/installation/ 

icons : https://ionicframework.com/docs/v2/ionicons/ 
push : https://docs.ionic.io/services/push/ 
push : https://medium.com/@ankushaggarwal/push-notifications-in-ionic-2-658461108c59#.l7dh5evsv 
push : http://nishanthkabra.com/ionic2push.html 
theme : http://ionicframework.com/docs/v2/theming/overriding-ionic-variables/ 
component : http://ionicframework.com/docs/v2/components/#overview 

 
init project :  
 
ionic start cutePuppyPics --v2					> start new project   
cd cutePuppyPics											 
ionic serve										> test web project 
cordova platform add android --save				> add android platform to project 
ionic platform android							> add android platform to project 
ionic run android  								> run project on android device 
 
ionic info 
 
generate elements 
ionic g page login 
ionic g provider MyData 

 
plugins :  
ionic plugin add cordova-plugin-geolocation 
ionic plugin add cordova-plugin-facebook4 --save --variable APP_ID="0105334862864787" --variable APP_NAME="APP-NAME" 
ionic plugin add cordova-plugin-whitelist 

 
facebook  
http://ionicframework.com/docs/v2/native/facebook/ 
https://github.com/fuffenz/ionic2-native-facebook-login 
cordova plugin add cordova-plugin-facebook4 --save --variable APP_ID="0105334862864787" --variable APP_NAME="APP-NAME" 
ionic plugin add cordova-plugin-facebook4 --save --variable APP_ID="0105334862864787" --variable APP_NAME="APP-NAME"
::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::::: 
 
  
## syntax
typescript types		https://www.typescriptlang.org/docs/handbook/basic-types.html 
typescript tuto 		http://www.typescriptlang.org/docs/tutorial.html interface vs classe 
typescript interface 	https://www.typescriptlang.org/docs/handbook/interfaces.html 
typescript classe 		http://www.typescriptlang.org/docs/handbook/classes.html 
typescript .d.t			https://github.com/DefinitelyTyped/DefinitelyTyped 		/// <reference path="angular.d.ts" /> 
typescript arrays		http://www.codecompiled.com/arrays-in-typescript/ 
 
typescript interface 	interface HasScore {   score: number; }     function addPointsToScore(player: HasScore, points: number): void {       player.score += points;     } 
typescript interface	interface CanRun {   run(meters: number): void; }     function startRunning(pony: CanRun): void {       pony.run(10);     } 
typescript classe		class NamedPony {   constructor(public name: string, private speed: number) {   } 
 
typescript optionnal 	public votes?: number; 		+ this.votes = votes || 0; 
typescript types 		const poneyNumber: number = 0; 	const poneyName: string = 'Rainbow Dash';  
						const pony: Pony = new Pony(); const ponies: Array<Pony> = [new Pony()]; 
typescript type retour  function startRace(race: Race): Race {  
typescript enum			enum RaceStatus {Ready, Started, Done}     const race = new Race();     race.status = RaceStatus.Ready; 
		 
es6 features			http://es6-features.org/#Constants		 
es6 collections 		const users = new Map(); OU const users = new Set(); 
es6 iterer				for (let user of users) {   console.log(user.name); } 
es6 template 		 	const fullname = `Miss ${firstname} ${lastname}`; 

 
 
classe ou interface -> 
classe si besoin de creer des function sur le pojo ou bien interface suffit 
si classe alors utiliser mecanisme fromJSON (ng-book2 screencast final-app voir code source) 
 
rxJs  https://xgrommx.github.io/rx-book/index.html + http://rxmarbles.com/ 
le listener = un observer 
le flux = un observable (collection asynchrone dont les événements arrivent au cours du temps) 
 
• take(n) va piocher les n premiers éléments.  
• map(fn) va appliquer la fonction fn sur chaque événement et retourner le résultat.  
• filter(predicate) laissera passer les seuls événements qui répondent positivement au prédicat.  
• reduce(fn) appliquera la fonction fn à chaque événement pour réduire le flux à une seule valeur unique.  
• merge(s1, s2) fusionnera les deux flux.  
• subscribe(fn) appliquera la fonction fn à chaque événement qu’elle reçoit. 
• forEach(fn) 
 
• transformation (delaying, debouncing…) 
• combinaison (merge, zip, combineLatest…)  
• filtrage (distinct, filter, last…)  
• mathématique (min, max, average, reduce…)  
• conditions (amb, includes…) 
 
EventEmitter (Angular2 : adapter Observable)  EventEmitter a une méthode subscribe() pour réagir aux événements, et cette méthode reçoit trois paramètres : 
• une méthode pour réagir aux événements. 
• une méthode pour réagir aux erreurs.  
• une méthode pour réagir à la terminaison. 
Un EventEmitter peut émettre un événement avec la méthode emit(). 
 
const emitter = new EventEmitter(); 
const subscription = emitter.subscribe(   value => console.log(value),   error => console.log(error),   () => console.log('done') ); 
emitter.emit('hello'); emitter.emit('there'); emitter.complete(); 
subscription.unsubscribe(); // unsubscribe  
// logs "hello", then "there", then "done" 

 
pipe 
{{ asyncGreeting | async } 
 
{{ birthday | date:'shortTime' }} 		<!-- will display '3:30 PM' -- 
{{ article.date() | date:'medium'}}		 
{{ birthday | date:'longDate' }}		<!-- will display 'July 16, 1986' --> 
{{ birthday | date:'dd/MM/yyyy' }}		 
 
{{ ponies | json }} 
{{ ponies | slice:0:2 | json } 
{{ 'Ninja Squad' | uppercase }} 
{{ 'Ninja Squad' | lowercase }}	 
{{ 12345 | number:'.2' }			<!-- will display '12,345.00' --> 
{{ 12345.13 | number:'.1-1' }}		<!-- will display '12,345.1' --> 
{{ 0.8 | percent }} 				<!-- will display '80%' --> 
{{ 0.8 | percent:'.3' }} 			<!-- will display '80.000%' --> 
{{ 10.6 | currency:'EUR' }			<!-- will display 'EUR10.60' -->	 
 
<div *ngFor="let pony of ponies | slice:0:2">{{pony.name}}</div> 
<div loggable [logText]="expression | uppercase">Hello</div> 
 
ngTemplate  
<h2>Welcome {{user?.name}}</h2> 
 
ngIf 
<div *ngIf="races.length > 0"><h2>Races</h2></div> 
 
ngFor 
<ul> <li *ngFor="let race of races; let i=index">{{i}} - {{race.name}}</li> </ul> 
<ul> <li *ngFor="let article of articles | async">{{article.name}}</li> </ul> 
 
ngFor + input class/bean 
<app-article *ngFor="let article of articles" [article]="article"></app-article> 
export class ArticleComponent { 
	@Input() article: Article; 
} 
 
ngSwitch 
<div [ngSwitch]="messageCount">   <p *ngSwitchCase="0">You have no message</p>   <p *ngSwitchCase="1">You have a message</p>   <p *ngSwitchDefault>You have some messages</p> </div> 
 
ngStyle 		La clé peut être en camelCase (fontWeight) ou en dash-case ('font-weight') 
<p [style.color]="foreground">Friendship is Magic</p>														> 1 atrribut 
<div [ngStyle]="{fontWeight: fontWeight, color: color}">I've got style</div>								> x atrributs 
 
ngClass 
<div [class.awesome-div]="isAnAwesomeDiv()">I've got style</div>											> 1 classe 
<div [ngClass]="{'awesome-div': isAnAwesomeDiv(), 'colored-div': isAColoredDiv()}">I've got style</div>		> x classes 
 
 
attribute input == binding de propriété 
<ns-pony name="{{pony.name}}"></ns-pony> === <ns-pony [name]="pony.name"></ns-pony> 
<ns-pony name="Pony {{pony.name}}"></ns-pony> === <ns-pony [name]="'Pony ' + pony.name"></ns-pony> 
<ns-pony name="{{pony.fullName()}}"></ns-pony> === <ns-pony [name]="pony.fullName()"></ns-pony> 
<option [selected]="isPonySelected" value="Rainbow Dash">Rainbow Dash</option> 
<div [hidden]="isHidden">Hidden or not</div> 
<p [style.color]="foreground">Friendship is Magic</p> 
 
attribute output  == binding d'évenement 		 les événements qui se propagent vers le haut depuis le fond des composants enfants 
<button (click)="onButtonClick()">Click me!</button> 
<div (click)="onButtonClick()">   <button>Click me!</button> </div> 					-> fonctionne car propagation vers le haut 
<div (click)="onButtonClick($event)">   <button>Click me!</button> </div>				-> récupérer l'evenement 
onButtonClick(event) {   event.preventDefault();   event.stopPropagation(); }			-> stopper la propagation 
 
variable locale 
<input type="text" #name> {{ name.value }} 
<input type="text" #name> <button (click)="name.focus()">Focus the input</button> 
<google-youtube #player></google-youtube><button (click)="player.play()">Play!</button> 
 
DIRECTIVE  (une directive n’a pas de vue). 
selecteur: Ne nomme pas tes sélecteurs avec un préfixe bind-, on-, let- ou ref- : ils ont une autre signification pour le parseur, car ils font partie de la syntaxe canonique des templates. 
• un élément, comme c’est généralement le cas pour les composants : footer. 
• une classe, mais c’est plutôt rare : .alert.  
• un attribut, ce qui est le plus fréquent pour une directive : [color].  
• un attribut avec une valeur spécifique : [color=red].  
• une combinaison de ceux précédents : footer[color=red] désignera un élément footer avec un attribut color à la valeur red.  
 
@Directive({    
selector: '[loggable]',    
inputs: ['text: logText']  
})  
export class SimpleTextWithSetterDirective { 
  	set text(value) {     console.log(value);   }  
} 
	OU  
	 
@Directive({    
selector: '[loggable]'  
})  
export class InputDecoratorOnSetterDirective { 
  	@Input('logText')    
	set text(value) {     console.log(value);   }  
} 
 
 
cycle de vie 
• ngOnChanges sera la première appelée quand la valeur d’une propriété bindée est modifiée. Elle recevra une map changes, contenant les valeurs courante et précédente du binding, emballées dans un SimpleChange. Elle ne sera pas appelée s’il n’y a pas de changement.  
• ngOnInit sera appelée une seule fois après le premier changement (alors que ngOnChanges est appelée à chaque changement). Cela en fait la phase parfaite pour du travail d’initialisation, comme son nom le laisse à penser.  
• ngOnDestroy est appelée quand le composant est supprimé. Utile pour y faire du nettoyage. 
• ngDoCheck est légèrement différente. Si elle est présente, elle sera appelée à chaque cycle de détection de changements, redéfinissant l’algorithme par défaut de détection, qui inspecte les différences pour chaque valeur de propriété bindée. Cela signifie que si une propriété au moins est modifiée, le composant est considéré modifié par défaut, et ses enfants seront inspectés et réaffichés. Mais tu peux redéfinir cela si tu sais que la modification de certaines entrées n’a pas de conséquence. Cela peut être utile si tu veux accélérer le cycle de détection de changements en n’inspectant que le minimum, mais en règle générale tu ne devrais pas avoir à le faire.  
• ngAfterContentInit est appelée quand tous les bindings du composant ont été vérifiés pour la première fois.  
• ngAfterContentChecked est appelée quand tous les bindings du composant ont été vérifiés, même s’ils n’ont pas changé.  
• ngAfterViewInit est appelée quand tous les bindings des directives enfants ont été vérifiés pour la première fois.  
• ngAfterViewChecked est appelée quand tous les bindings des directives enfants ont été vérifiés, 
même s’ils n’ont pas changé. Cela peut être utile si ton composant attend quelque chose de ses composants enfants. Comme ngAfterViewInit, cela n’a de sens que pour un composant (une directive n’a pas de vue). 

 
ajouter un fichier css ou lib js : 
- installer via npm --save 
- ajouter dans angular-cli.json > balises styles + scripts 

 
résumé  
{{}} pour l’interpolation,  
[] pour le binding de propriété (entrée) 
() pour le binding d’événement (sortie) 
# pour la déclaration de variable 
* pour les directives structurelles 
 
testing 
 
cas sans asynchrone (promise/observable) 
 
import { TestBed } from '@angular/core/testing'; 
describe('RaceService', () => {    
	let service: RaceService; 
  	beforeEach(() => TestBed.configureTestingModule({     providers: [RaceService]   })); 
  	beforeEach(() => service = TestBed.get(RaceService)); 
  	it('should return races when list() is called', () => {       
		expect(service.list().length).toBe(2);    
	});  
}); 

 
cas avec asynchorne (promise/observable) 
 
import { async, TestBed } from '@angular/core/testing'; 
describe('RaceService', () => {   let service: RaceService; 
  beforeEach(() => TestBed.configureTestingModule({     providers: [RaceService]   })); 
  beforeEach(() => service = TestBed.get(RaceService)); 
  it('should return a promise of 2 races', async(() => { 
     service.list().then(races => { 
       expect(races.length).toBe(2);      
	 });    
 }));  
}); 
  
cas espionner appel et remplacer par factice 
 
import { TestBed } from '@angular/core/testing'; 
describe('RaceService', () => { 
  const localStorage = jasmine.createSpyObj('LocalStorageService', ['get']); 
  beforeEach(() => TestBed.configureTestingModule({     providers: [       { provide: LocalStorageService, useValue: localStorage },       RaceService     ]   })); 
  it('should return 2 races from localStorage', () => {      
	localStorage.get.and.returnValue([{ name: 'Lyon' }, { name: 'London' }]); 
    const service = TestBed.get(RaceService);      
	const races = service.list(); 
    expect(races.length).toBe(2);      
	expect(localStorage.get).toHaveBeenCalledWith('races');    
  });  
}); 
 
test end to end (voir ninja angular page 157) 