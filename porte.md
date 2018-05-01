---
title: Porte d'entrée
description: Pose ou remplacement de porte d'entrée
permalink: /porte/
form:
<article id="formArticle">

			<div id="progress" class="row" [hidden]="formState.currentStep > 3">
				<div class="four columns barText" [text]="'Étape ' + (formState.currentStep+1) + '/4'">Étape 4/4</div>
				<div class="six columns barContainer">
					<div class="barValue step3" [class]="'barValue step' + formState.currentStep">&nbsp;</div>
				</div>
			</div>

      <form id="formGroup" method="post" action-xhr="https://travorama.fr/api/submit/" on="submit:AMP.setState({ formState: { submitted: formState.currentStep >= 3 } });submit-success:AMP.setState({ formState: { currentStep: formState.currentStep + 1, submitted: false } }),formArticle.scrollTo(position=top);submit-error:AMP.setState({ formState: { submitted: false } })" custom-validation-reporting="show-first-on-submit" target="_top" novalidate="" class="i-amphtml-form user-valid amp-form-submit-success">

				<input type="hidden" name="landing" id="landing" value="porte" class="user-valid valid">
				<input type="hidden" name="currentStep" id="currentStep" value="3" [value]="formState.currentStep.toString()" class="user-valid valid">

				<section [hidden]="formState.currentStep != 0" hidden="">

					

          
          <fieldset class="user-valid valid">
  <legend>
    Type de travaux
    <span visible-when-invalid="valueMissing" validation-for="id_work_type__new">Obligatoire</span>
  </legend>
  
  <div class="row">
    
    <label for="id_work_type__new" class="radio six columns">
      <input type="radio" name="work_type" id="id_work_type__new" value="new" required="" [required]="formState.currentStep >= 0" class="user-valid valid">
      <span class="label-body">Installation neuve</span>
    </label>
    
    <label for="id_work_type__rep" class="radio six columns">
      <input type="radio" name="work_type" id="id_work_type__rep" value="rep" required="" [required]="formState.currentStep >= 0" class="user-valid valid">
      <span class="label-body">Remplacement</span>
    </label>
    
  </div>
  
</fieldset>
          

          
          <label for="id_number">Nombre de portes</label>
<select name="number" id="id_number" class="user-valid valid">
  
  <option value="1">1</option>
  
  <option value="2">2</option>
  
  <option value="3m">3 ou plus</option>
  
</select>
          

          
          <label for="id_category">Type de porte</label>
<select class="u-full-width user-valid valid" name="category" id="id_category">
  
  <option value="1287">Porte blindée</option>
  
  <option value="1282">Porte en acier</option>
  
  <option value="1280">Porte en aluminum</option>
  
  <option value="1279">Porte en bois</option>
  
  <option value="1283">Porte en PVC</option>
  
  <option value="1281">Porte en verre</option>
  
  <option value="1911">Je souhaite que l'on me conseille</option>
  
</select>
          



				</section>

				<section [hidden]="formState.currentStep != 1" hidden="">

					

          
          <fieldset class="user-valid valid">
  <legend>
    Type de prestation
    <span visible-when-invalid="valueMissing" validation-for="id_service_type__supply_install">Obligatoire</span>
  </legend>
  
  <div class="row">
    
    <label for="id_service_type__supply_install" class="radio six columns">
      <input type="radio" name="service_type" id="id_service_type__supply_install" value="supply_install" [required]="formState.currentStep >= 1" class="user-valid valid" required="">
      <span class="label-body">Fourniture et pose</span>
    </label>
    
    <label for="id_service_type__supply" class="radio six columns">
      <input type="radio" name="service_type" id="id_service_type__supply" value="supply" [required]="formState.currentStep >= 1" class="user-valid valid" required="">
      <span class="label-body">Fourniture seule</span>
    </label>
    
  </div>
  
  <div class="row">
    
    <label for="id_service_type__install" class="radio six columns">
      <input type="radio" name="service_type" id="id_service_type__install" value="install" [required]="formState.currentStep >= 1" class="user-valid valid" required="">
      <span class="label-body">Pose seule</span>
    </label>
    
  </div>
  
</fieldset>
          



					
          <label for="id_objective">Objectif de ma demande</label>
<select class="u-full-width user-valid valid" name="objective" id="id_objective">
  
  <option value="e+c">Je veux comparer des devis et choisir un artisan</option>
  
  <option value="c">J'ai besoin de trouver un artisan</option>
  
  <option value="e">J'aimerais avoir un devis pour connaître les prix</option>
  
</select>
          

					
          <fieldset class="user-valid valid">
  <legend>
    Je souhaite qu'un artisan intervienne
    <span visible-when-invalid="valueMissing" validation-for="id_delay__asap">Obligatoire</span>
  </legend>
  
  <div class="row">
    
    <label for="id_delay__asap" class="radio six columns">
      <input type="radio" name="delay" id="id_delay__asap" value="asap" [required]="formState.currentStep >= 1" class="user-valid valid" required="">
      <span class="label-body">dès que possible</span>
    </label>
    
    <label for="id_delay__1y" class="radio six columns">
      <input type="radio" name="delay" id="id_delay__1y" value="1y" [required]="formState.currentStep >= 1" class="user-valid valid" required="">
      <span class="label-body">dans l'année</span>
    </label>
    
  </div>
  
  <div class="row">
    
    <label for="id_delay__3m" class="radio six columns">
      <input type="radio" name="delay" id="id_delay__3m" value="3m" [required]="formState.currentStep >= 1" class="user-valid valid" required="">
      <span class="label-body">dans moins de 3 mois</span>
    </label>
    
    <label for="id_delay__undefined" class="radio six columns">
      <input type="radio" name="delay" id="id_delay__undefined" value="undefined" [required]="formState.currentStep >= 1" class="user-valid valid" required="">
      <span class="label-body">pas de date fixée</span>
    </label>
    
  </div>
  
  <div class="row">
    
    <label for="id_delay__6m" class="radio six columns">
      <input type="radio" name="delay" id="id_delay__6m" value="6m" [required]="formState.currentStep >= 1" class="user-valid valid" required="">
      <span class="label-body">dans moins de 6 mois</span>
    </label>
    
  </div>
  
</fieldset>
          

				</section>

        <section [hidden]="formState.currentStep != 2" hidden="">

          <label for="id_user_type">Je suis</label>
          <div class="row">
            <select class="six columns user-valid valid" id="id_user_type" name="user_type">
							
							<option value="individual">un particulier</option>
							
							<option value="company">une entreprise</option>
							
							<option value="shop">un commerçant</option>
							
							<option value="syndic">un syndic de copropriété</option>
							
							<option value="architect">un architecte</option>
							
							<option value="association">une association</option>
							
							<option value="realestate">une agence immobilière</option>
							
							<option value="other">autre</option>
							
            </select>
            <select class="six columns user-valid valid" id="id_user_function" name="user_function">
							
							<option value="owner">propriétaire occupant</option>
							
							<option value="landlord">propriétaire bailleur</option>
							
							<option value="proxy">mandaté par le(s) propriétaire(s)</option>
							
							<option value="futureowner">futur propriétaire</option>
							
							<option value="tenant">locataire</option>
							
							<option value="futuretenant">futur locataire</option>
							
							<option value="other">autre</option>
							
            </select>
          </div>

					

          
          <fieldset class="user-valid valid">
  <legend>
    Type de bien
    <span visible-when-invalid="valueMissing" validation-for="id_home_type__house" class="">Obligatoire</span>
  </legend>
  
  <div class="row">
    
    <label for="id_home_type__house" class="radio six columns">
      <input type="radio" name="home_type" id="id_home_type__house" value="house" [required]="formState.currentStep >= 2" class="user-valid valid" required="">
      <span class="label-body">Maison individuelle</span>
    </label>
    
    <label for="id_home_type__shop" class="radio six columns">
      <input type="radio" name="home_type" id="id_home_type__shop" value="shop" [required]="formState.currentStep >= 2" class="user-valid valid" required="">
      <span class="label-body">Commerce</span>
    </label>
    
  </div>
  
  <div class="row">
    
    <label for="id_home_type__flat" class="radio six columns">
      <input type="radio" name="home_type" id="id_home_type__flat" value="flat" [required]="formState.currentStep >= 2" class="user-valid valid" required="">
      <span class="label-body">Appartement</span>
    </label>
    
    <label for="id_home_type__other" class="radio six columns">
      <input type="radio" name="home_type" id="id_home_type__other" value="other" [required]="formState.currentStep >= 2" class="user-valid valid" required="">
      <span class="label-body">Autre</span>
    </label>
    
  </div>
  
  <div class="row">
    
    <label for="id_home_type__office" class="radio six columns">
      <input type="radio" name="home_type" id="id_home_type__office" value="office" [required]="formState.currentStep >= 2" class="user-valid valid" required="">
      <span class="label-body">Bureau</span>
    </label>
    
  </div>
  
</fieldset>
          



					<div class="row">
						<div class="five columns">
		          <label for="id_postal_code">
								Lieu des travaux
								<span visible-when-invalid="valueMissing" validation-for="id_postal_code">Obligatoire</span>
								<span visible-when-invalid="patternMismatch" validation-for="id_postal_code">Invalide</span>
							</label>
		          <input id="id_postal_code" class="u-full-width user-valid valid" type="text" placeholder="Code postal" name="postal_code" maxlength="5" pattern="^(([1345678][0-9])|([02][1-9])|(9[0-5]))[0-9]{3}$" on="input-throttled:AMP.setState({ formState: {postalCode: event.value.charAt(4)?event.value:'', city: ''} })" [required]="formState.currentStep == 2">
						</div>
						<div class="seven columns">
							<amp-list layout="fixed-height" height="10rem" src="https://travorama.fr/api/cities/?postal_code=92100" [src]="'https://travorama.fr/api/cities/?postal_code=' + formState.postalCode" class="i-amphtml-element i-amphtml-layout-fixed-height i-amphtml-layout-size-defined i-amphtml-layout" style="height: 10rem;" aria-live="polite">
								<template type="amp-mustache">
									<label for="id_city">
										Ville
										{{^cities}}{{#postalCode}}<span class="cityError">Aucune ville ne correspond</span>{{/postalCode}}{{/cities}}
										{{^singleton}}{{#cities.length}}<span class="valueMissing" [hidden]="formState.city != ''">Obligatoire</span>{{/cities.length}}{{/singleton}}
									</label>
									<select class="u-full-width" id="id_city" name="city" on="change:AMP.setState({ formState: { city: event.value }})">
										{{^singleton}}{{#cities.length}}<option value="" disabled="" selected="" hidden="">Choisissez...</option>{{/cities.length}}{{/singleton}}
										{{#cities}}<option>{{name}}</option>{{/cities}}
									</select>
								</template>
							<div class="i-amphtml-fill-content i-amphtml-replaced-content" role="list"><div role="listitem">
									<label for="id_city">
										Ville
										
										
									</label>
									<select class="u-full-width user-valid valid" id="id_city" name="city" on="change:AMP.setState({ formState: { city: event.value }})">
										
										<option>Boulogne-Billancourt</option>
									</select>
								</div></div><div class="i-amphtml-loading-container i-amphtml-fill-content amp-hidden"><div class="i-amphtml-loader">
        <div class="i-amphtml-loader-dot"></div>
        <div class="i-amphtml-loader-dot"></div>
        <div class="i-amphtml-loader-dot"></div>
      </div></div></amp-list>
						</div>
					</div>

				</section>

        <section [hidden]="formState.currentStep != 3">

					
          <fieldset class="user-valid valid">
  <legend>
    Civilité
    <span visible-when-invalid="valueMissing" validation-for="id_salutation__ms">Obligatoire</span>
  </legend>
  
  <div class="row">
    
    <label for="id_salutation__ms" class="radio six columns">
      <input type="radio" name="salutation" id="id_salutation__ms" value="ms" [required]="formState.currentStep >= 3" class="user-valid valid" required="">
      <span class="label-body">Madame</span>
    </label>
    
    <label for="id_salutation__mr" class="radio six columns">
      <input type="radio" name="salutation" id="id_salutation__mr" value="mr" [required]="formState.currentStep >= 3" class="user-valid valid" required="">
      <span class="label-body">Monsieur</span>
    </label>
    
  </div>
  
</fieldset>
          

					<div class="row">
						<div class="six columns">
							<label for="id_lastname">
								Nom
								<span visible-when-invalid="valueMissing" validation-for="id_lastname">Obligatoire</span>
							</label>
							<input class="u-full-width user-valid valid" type="text" placeholder="Lorrain" id="id_lastname" name="lastname" [required]="formState.currentStep == 3" required="">
						</div>
						<div class="six columns">
							<label for="id_firstname">
								Prénom
								<span visible-when-invalid="valueMissing" validation-for="id_firstname">Obligatoire</span>
							</label>
							<input class="u-full-width user-valid valid" type="text" placeholder="Claude" id="id_firstname" name="firstname" [required]="formState.currentStep == 3" required="">
						</div>
					</div>

					<label for="id_email">
						Adresse électronique
						<span visible-when-invalid="valueMissing" validation-for="id_email">Obligatoire</span>
						<span visible-when-invalid="patternMismatch" validation-for="id_email">Invalide</span>
					</label>
					<input id="id_email" name="email" class="u-full-width user-valid valid" type="text" pattern="^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,4}$" placeholder="claude.lorrain@exemple.fr" [required]="formState.currentStep == 3" required="">

					<label for="id_phone">
						Numéro de téléphone
					</label>
					<div class="row">
						<input id="id_phone" name="phone" type="tel" placeholder="Téléphone" pattern="(?:0|\(?\+33\)?\s?|0033\s?)[1-79](?:[\.\-\s]?\d\d){4}$" maxlength="20" [required]="formState.currentStep == 3" class="user-valid valid" required="">
						<span visible-when-invalid="valueMissing" validation-for="id_phone" class="phoneError">Obligatoire</span>
						<span visible-when-invalid="patternMismatch" validation-for="id_phone" class="phoneError">Invalide</span>
					</div>

					
					<label for="id_description">Précisons sur les travaux à mener</label>
					<textarea class="u-full-width user-valid valid" id="id_description" name="description" placeholder="Je cherche un professionnel qualifié..."></textarea>
					

					<fieldset class="user-valid valid">
						<label for="id_cgv">
							<input id="id_cgv" name="cgv" type="checkbox" [required]="formState.currentStep == 3" class="user-valid valid" required="">
							<span>J'ai lu et j'accepte <a target="_blank" href="https://www.homly-you.com/cgv">les conditions générales d'utilisation</a> du service gratuit de mise en relation Homly You en partenariat avec Travorama.</span>
							<span visible-when-invalid="valueMissing" validation-for="id_cgv">L'acceptation des conditions générales est nécessaire pour poursuivre</span>
						</label>
					</fieldset>

				</section>

				<section hidden="" [hidden]="formState.currentStep != 4">

					<amp-img src="https://travorama.fr/static/fa-thumbs-up.svg" id="requestSaved" height="3em" noloading="" class="i-amphtml-element i-amphtml-layout-fixed-height i-amphtml-layout-size-defined" style="height: 3em;"></amp-img>
					<h2>Demande enregistrée !</h2>
					<p>Votre demande a été prise en compte. Un conseiller Homly You vous rappellera dès que possible.</p>
					<p>Cordialement,</p>
					<p>L'équipe Travorama et Homly You</p>

				</section>

				<div class="section alert" submit-error="">
					<template type="amp-mustache">
						{{message}}
					</template>
				</div>

				<section [hidden]="formState.currentStep == 4">
					<div class="buttonGroup" [hidden]="formState.submitted">
						<div id="formBackButton" class="button" [hidden]="formState.currentStep==0" role="button" tabindex="0" on="tap:AMP.setState({ formState: { 'currentStep': formState.currentStep - 1 } }),formArticle.scrollTo(position=top)">Revenir</div>
						<input id="formNextButton" class="button-primary user-valid valid" [hidden]="formState.currentStep == 3" type="submit" value="Continuer" hidden="">
						<input id="formSaveButton" class="button-primary user-valid valid" [hidden]="formState.currentStep < 3" type="submit" value="Terminer">
					</div>
					<div class="buttonGroup" hidden="" [hidden]="!formState.submitted">
						Veuillez patienter...
					</div>
				</section>

				<amp-analytics data-consent-notification-id="cookieConsent" type="googleadwords" class="i-amphtml-element i-amphtml-layout-fixed i-amphtml-layout-size-defined i-amphtml-layout" style="width: 1px; height: 1px; display: none;" aria-hidden="true">
					<script type="application/json">
						{
						  "triggers": {
						    "onRequestSaved": {
									"selector": "#requestSaved",
						      "on": "visible",
						      "request": "conversion"
								}
						  },
							"vars": {
								"googleConversionId": "810372056",
								"googleConversionLanguage": "fr",
								"googleConversionFormat": "3",
								"googleConversionLabel": "Kws-COqZ3n8Q2Je1ggM",
								"googleRemarketingOnly": "false"
							}
						}
					</script>
				</amp-analytics>
				<amp-analytics data-consent-notification-id="cookieConsent" type="googleanalytics" class="i-amphtml-element i-amphtml-layout-fixed i-amphtml-layout-size-defined i-amphtml-layout" style="width: 1px; height: 1px; display: none;" aria-hidden="true">
					<script type="application/json">
						{
							"triggers": {
								"formSubmission": {
									"on": "amp-form-submit",
									"request": "event",
									"vars": {
										"eventCategory": "funnel tracking",
										"eventAction": "submit currentStep=${formFields[currentStep]}"
									}
								},
								"formBack": {
									"on": "click",
									"selector": "#formBackButton",
									"request": "event",
									"vars": {
										"eventCategory": "funnel tracking",
										"eventAction": "goBack"
									}
								},
								"requestSaved": {
									"selector": "#requestSaved",
						      "on": "visible",
									"request": "event",
									"vars": {
										"eventCategory": "funnel tracking",
										"eventAction": "conversion"
									}
								},
								"trackPageview": {
									"on": "visible",
									"request": "pageview"
								}
							},
							"vars": {
								"account": "UA-66880357-27",
								"eventLabel": "${title}",
								"anonymizeIP": "aip" 
							}
						}
					</script>
				</amp-analytics>

      </form>

			<footer>
				<p>
					 <a target="_blank" href="https://travorama.fr/legal.html">Mentions légales - CGU</a>
				</p>
				<p hidden="" [hidden]="formState.currentStep != 4">
					Icône "thumbs up" réalisée par <a href="https://fontawesome.com/">FontAwesome</a> sous <a href="https://fontawesome.com/license">license CC BY 4.0</a>
				</p>
		  </footer>

    </article>


---

On l’utilise souvent sans s’en rendre compte, et pourtant, elle exerce une fonction importante dans le logement. De la protection contre les infractions, à l’isolation thermique, en passant par une fonction décorative : vous l’avez bien compris, il s’agit de la porte d'entrée !

Vous trouverez ci-dessous tous les trucs et astuces ainsi que nos conseil pour bien choisir sa porte d'entrée adaptée à ses besoins.

## Checklist des points à vérifier avant de poser sa porte d'entrée

Beaucoup de questions sont à répondre quand on fait poser une nouvelle porte d'entrée :
1. L’esthétique
2. Les dimensions
3. Le matériau
4. La sécurité attendue
5. Les performances thermiques et acoustiques

### Dimensions

Les portes sont de manière générale d’une dimension standard définie par les vantaux afin de répondre à des critères d’accessibilité. Elles font de manière générale 215 x 90 cm mais il existe d’autres dimensions standards :
200 x 90 cm et 200 x 80 cm. Il peut arriver que pour des rénovations, les dimensions des portes d’entrée anciennes ne soient pas standardisées.
Ainsi, on peut se retrouver à devoir procéder à la pose d’une porte d'entrée sur-mesure.
Dans tous les cas, contactez des pros compétents susceptibles de pouvoir vous fournir des devis détaillés et adaptés à votre budget pour un moindre coût !

### Matériaux

Concernant les matériaux, on retrouve des composants classiques tels que le bois ou l’aluminium, mais il existe aussi le PVC ou les matériaux composites.
Chacun possède ses propres avantages, dont voici un bref résumé :
1. Porte d'entrée en bois : robuste et propose une belle performance en terme d’isolation thermique et acoustique, et durable.
2. Porte d'entrée en aluminium : extrêmement robuste donc idéal pour une sécurité accrue mais peu efficace en terme d’isolation thermique.
3. Porte d'entrée en PVC : la solution la moins chère qui répondra à tous vos besoins, par contre, pas hyper sécu.
4. Porte d'entrée en matériaux composites : c’est la meilleure solution si vous voulez allier robustesse et performance énergétique.
5. Porte d'entrée en bois-alu : tous les avantages du bois et de l’alu

### La sécurité

La sécurité est primordiale pour une porte d'entrée. C’est pourquoi, optez pour un maximum de sécurité avec les portes blindées. Choisissez bien le nombre de points de la serrure (3 ou 6). Si vous voulez une porte d'entrée blindée sécurisée,
faites appel à un professionnel pour vous assurer de la bonne installation de la porte d'entrée.

### Isolation thermique et acoustique

Conserver la chaleur donnée par le foyer est une des fonctions essentiellesde la porte d'entrée. Les performances thermiques d’une porte sont définies par le coefficient Ud : plus celui-ci sera faible et proche de 1, plus la porte sera isolante.

Attention toutefois lors d’une rénovation à bien vérifier les gonds. Si vous voulez optimiser l’isolation thermique et acoustique de votre porte d’entrée, mieux vaut poser un nouveau bloc et un nouveau seuil étanche.

Faites appel à un bon artisan compétent pour ces travaux d’installation de porte d'entrée.

## Comparez les devis de pose de porte d'entée</h2>

### Combien coute la pose d’une porte d'entrée ?

Le coût du remplacement dépend de beaucoup de paramètres : difficulté du chantier, la durée, le type de porte souhaité (matériau) ainsi que la région dans laquelle se situe le chantier. Si certains sites proposent des devis en ligne gratuits, mieux vaut faire appel à un professionnel du bâtiment qualifié.
Il saura mieux répondre à vos besoins.

### Que faut-il vérifier sur un devis de pose de porte d'entrée ?</h3>

Assurez-vous que les informations suivantes soient bien présentes :
1. Le Pro soit RGE
2. Les performances de la porte (Ud) soient bien présentes
3. La fourniture du matériel et la TVA soient bien pris en compte dans le devis

Avec toutes ces infos, vous êtes maintenant capable de trouver le bon pro pour vos travaux : il saura répondre parfaitement à vos besoins de pose de porte d'entrée au meilleur prix.
	


