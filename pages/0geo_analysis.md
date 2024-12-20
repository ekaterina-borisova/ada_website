---
title: Geographical Analysis
layout: post
description: 'Geographical Analysis'
image: assets/images/geo_analysis.jpg
nav-menu: true
---

 What impact does geography have on the development of drugs? Specifically, does a drug's origin matter in drug-drug interaction? The development of pharmaceuticals is a collaborative effort that often reflects the expertise and innovation of the institutions behind them. This project aims to investigate whether drugs developed within the same institutions exhibit superior interaction profiles compared to those developed independently. One may hypothesise that shared research environments, methodologies, and collaborative networks contribute to a higher likelihood of favorable interactions among drugs originating from the same institution.

 Another question one could pose is whether the prevalence of a disease in a region has an effect on local drug development? The world is highly interconnected and an outbreak of any disease anywhere is today a menace for the whole world. Are there however any trends one can observe in the location of drug research with respect to the geographical prevalence of a disease?

<!-- Main -->
<div id="main">

<section id="one">
	<div class="inner">
		<header class="major">
			<h2>Some Analysis on BindingDB Dataset</h2>
		</header>
		<p>To answer these questions, we use the BindingDB dataset. It provides information on the interactions between proteins and ligands, focusing on binding affinity data. It contains 2,937,206 results on 1,295,089 ligands and 6746 targets. In total, there are 330 different source organisms for the targets. BindingDB provides a plethora of data for each experiment, there are 194 columns. For each experiment, we have the binding affinities constants such as Ki, Kd, IC50 and EC50, we have the ligand’s SMILES representation, the target name, the target source organism and the institution where the experiment was made. Since we want to make a geographical analysis of the trends of research, we focused on institutions that are located only in one country (some companies have multiple faculties in different countries).</p>
	</div>
</section>

<!-- Two -->
<section id="two" class="spotlights">
	<section>
		<a class="image">
			{% include countries_with_most_institutions.html %}
		</a>
		<div class="content">
			<div class="inner">
				<p>The graph shows that the United States has the highest number of institutions conducting experiments listed in the dataset, followed by China, Germany, and Italy.</p>
			</div>
		</div>
	</section>
	<section>
		<a class="image">
			{% include top_countries_bar_chart.html %}
		</a>
		<div class="content">
			<div class="inner">
				<p>Based on the graph, the USA has conducted the highest number of experiments listed in the dataset, totaling approximately 380,000. China follows with around 150,000 experiments, while Germany and Italy are next, each contributing roughly 100,000 experiments.</p>
			</div>
		</div>
	</section>
	<section>
		<a class="image">
			{% include continents_pie.html %}
		</a>
		<div class="content">
			<div class="inner">
				<p>The graph indicates that Europe has the highest proportion of institutions conducting experiments in the dataset, with 39.4%. Asia follows with 29.0%, and North America accounts for 26.8%.</p>
			</div>
		</div>
	</section>
		<section>
		<a class="image">
			{% include contribs_by_continents_pie.html %}
		</a>
		<div class="content">
			<div class="inner">
				<p>The graph shows that 39.2% of the experiments were conducted in North America, 34.3% in Europe, and 23.5% in Asia, while only 3% took place in Africa, Oceania, and South America combined.</p>
			</div>
		</div>
	</section>
</section>

<section id="one">
    <div class="inner">
        <header class="major">
            <h3>World institutions heatmap</h3>
        </header>
        <div class="map-container" style="position: relative; width: 100%; height: 600px;">
            <iframe 
                src="../assets/geo_analysis_heatmaps/map.html" 
                style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none;">
            </iframe>
        </div>
    </div>
	<div class="inner">
		 <p>This heatmap shows the geographical distribution of institutions conducting experiments in the BindingDB dataset. It is a visual confirmation of our previous observations, the contributions to the dataset are driven by a few hotspots. </p>
		
	</div>
</section>
<!-- <section id="one">
    <div class="inner">
        <header class="major">
            <h2>World institutions heatmap</h2>
        </header>
        <div class="iframe-container" style="position: relative; width: 100%; max-width: 800px; height: 600px; margin: 0 auto;">
            <!-- Shadow DOM container 
            <div id="map-container" style="width: 100%; height: 100%; border: 1px solid #ccc; overflow: hidden;">
                <!-- Placeholder for map content 
                <!-- This content will be moved to the shadow DOM dynamically 
                <div id="map-content" style="display: none;">
                    {% include map.html %}
                </div>
            </div>
        </div>
    </div>
</section>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const container = document.getElementById('map-container');
    
    // Create shadow DOM to isolate the styles
    const shadow = container.attachShadow({mode: 'open'});
    
    // Get the content from the #map-content div
    const mapContent = document.getElementById('map-content').innerHTML;

    // Insert the map content into the shadow DOM
    shadow.innerHTML = `
      <style>
        :host {
          display: block;
          width: 100%;
          height: 100%;
        }
        /* Optional: Reset some inherited styles to prevent unwanted behavior */
        * {
          box-sizing: border-box;
        }
      </style>
      <div style="width: 100%; height: 100%;">
        ${mapContent}
      </div>
    `;
  });
</script> -->

<section id="one">
	<div class="inner">
		<p>In conclusion, the graphs show that the majority of research is conducted in Europe, North America, and Asia, and most research institutions are also located in these regions. They also show that the USA stands out as the country with the highest number of institutions conducting experiments and making the most contributions, followed by China in second place.</p>
	</div>
</section>

</div>

<br>

<!-- Main -->
<div id="main">

<section id="one">
	<div class="inner">
		<header class="major">
			<h2>Target based insights</h2>
		</header>
		<p>We want to have more insights on the target source organisms. For each target source organism (TSO), we calculated the proportion of experiments where the source organism for the target was specified. </p>
	</div>
</section>

<section id="two" class="spotlights">
	<section>
		<a class="image">
			{% include proportions_of_experiments_given_TSO.html %}
		</a>
		<div class="content">
			<div class="inner">
				<p>The graph shows that 81.6% of the experiments are conducted on targets derived from Homo sapiens (humans), followed by Rattus norvegicus (rats).</p>
			</div>
		</div>
	</section>
</section>

</div>

<br>
<br>

# Does the prevalence of a disease in a region drive the amount and focus of research conducted there?

<br>
<br>

<!-- Main -->
<div id="main">

<section id="one">
	<div class="inner">
		<header class="major">
			<h2>WHO database</h2>
		</header>
		<p>
			Up until now, we have analyzed the BindingDB database. To perform a comparative analysis of research output and disease prevalence, we need data on the prevalence of the diseases studied in the BindingDB dataset. For this purpose, we will use data from the World Health Organization (WHO), available at the following link: <a href="https://ghoapi.azureedge.net/api/" target="_blank">https://ghoapi.azureedge.net/api/</a>.
		</p>

		<p>
			After reviewing the WHO database, we identified eight diseases that appear in both the WHO and BindingDB datasets. These diseases are:
		</p>

		<ul>
			<li>Plasmodium falciparum</li>
			<li>Human Immunodeficiency Virus (HIV)</li>
			<li>Poliovirus</li>
			<li>Plasmodium vivax</li>
			<li>Mycobacterium tuberculosis</li>
			<li>Escherichia coli</li>
			<li>Hepatitis C</li>
			<li>Staphylococcus aureus</li>
		</ul>
	</div>
</section>

<!-- Two -->
<section id="two" class="spotlights">
	<section style="display: flex; flex-wrap: wrap; align-items: flex-start;">
		<div style="flex: 2;">
			<div style="width: 450px; height: 338px; overflow: hidden; margin-right: -50px;">
				<iframe 
					src="../assets/geo_analysis_heatmaps/who_heatmap.html" 
					style="
					width: 900px; 
					height: 676px;  
					transform: scale(0.5); 
					transform-origin: top left; 
					border: none;
					">
				</iframe>
			</div>
		</div>
		<div class="content">
			<div class="inner">
				<p>The heatmap shows the prevalences per capita of these diseases in different regions of the world in proportion to each other. We can for example observe that many diseases are more prevalent in regions such as Africa and Eastern Mediterranean, as opposed to the Americas and Western Pacific.</p>
			</div>
		</div>
	</section>
	<section style="display: flex; flex-wrap: wrap; align-items: flex-start;">
		<div style="flex: 2;">
			<div style="width: 450px; height: 338px; overflow: hidden; margin-right: -50px;">
				<iframe 
					src="../assets/geo_analysis_heatmaps/research_heatmap.html" 
					style="
					width: 900px; 
					height: 676px; 
					transform: scale(0.5); 
					transform-origin: top left; 
					border: none;
					">
				</iframe>
			</div>
		</div>
		<div class="content">
			<div class="inner">
				<p>The heatmap shows the number of research experiments on these diseases in different regions of the world in proportion to each other. The heatmap reveals that Africa has the least amount of research conducted on these diseases, while America leads with the most research. Europe comes in second. </p>
			</div>
		</div>
	</section>
</section>
<!-- Three -->
<section id="three">
	<div class="inner">
		<p>The heatmaps show that regions with a high prevalence of diseases, such as Africa and the Eastern Mediterranean, have the least research conducted on these diseases. In contrast, regions with lower prevalence, such as America and Europe, have the highest research output. This disparity may be due to regions with high disease prevalence lacking the necessary resources for research, while regions with lower prevalence have greater research capacity.  </p>
	</div>
</section>

</div>

<br>

<!-- Main -->
<div id="main">

<section id="one">
	<div class="inner">
		<header class="major">
			<h2>Prevalence-Research Analysis</h2>
		</header>
		<p>
			Having data on quantity of research and disease prevalence in different countries, we can now analyze the relationship between the two. The question of how the prevalence of a disease in a region drives the amount and focus of research conducted there can be answered by studying the correlation between the two datasets.
			For each disease, we depict below the prevalence of the given disease against the number of experiments conducted on it:
			<div id="plot_HIV" style="width: 100%; margin-left: -50px;">
				{% include plot_HIV.html %}
			</div>
			<br>
			<div id="plot_Plasmodium_falciparum" style="width: 100%; margin-left: -50px;">
				{% include plot_Plasmodium_falciparum.html %} 
			</div>
			<br>
			<div id="plot_Poliovirus" style="width: 100%; margin-left: -50px;">
				{% include plot_Poliovirus.html %}
			</div>
			<br>
			<div id="plot_Plasmodium_vivax" style="width: 100%; margin-left: -50px;">
				{% include plot_Plasmodium_vivax.html %} 
			</div>
			<br>
			<div id="plot_Tuberculosis" style="width: 100%; margin-left: -50px;">
				{% include plot_Tuberculosis.html %} 
			</div>
			<br>
			<div id="plot_Hepatitis_C" style="width: 100%; margin-left: -50px;">
				{% include plot_Hepatitis_C.html %} 
			</div>
			<br>
			<div id="plot_Escherichia_coli" style="width: 100%; margin-left: -50px;">
				{% include plot_Escherichia_coli.html %} 
			</div>
			<br>
			<div id="plot_Staphylococcus_aureus" style="width: 100%; margin-left: -50px;">
				{% include plot_Staphylococcus_aureus.html %}
			</div>
		</p>
	</div>
</section>

<!-- Three -->
<section id="three">
	<div class="inner">
		<p>From the graphs we observe that many countries with high prevalence of a disease do not necessarily have a high number of experiments conducted on it. On the other hand, countries with low prevalence of a disease can have a high number of experiments conducted on it. This makes sense, as many countries with high prevalence of a disease might not have the resources to conduct research on it, while countries with low prevalence might have the resources to conduct research on it.  </p>

		<p>
			To better quantify the relationship between prevalence and research, we perform a linear regression analysis on the data. We seek to find how well the prevalence of a disease in a region predicts the number of experiments conducted on it in that region. The results of the linear regression analysis are visualized in the following heatmap.
		</p>
	</div>
</section>

<!-- Two -->
<section id="two" class="spotlights">
	<section style="display: flex; flex-wrap: wrap; align-items: flex-start;">
		<div style="flex: 2;">
			<div style="width: 450px; height: 338px; overflow: hidden; margin-right: -50px;">
				<iframe 
					src="../assets/geo_analysis_heatmaps/region_region_heatmap.html" 
					style="
					width: 900px; 
					height: 676px;  
					transform: scale(0.5); 
					transform-origin: top left; 
					border: none;
					">
				</iframe>
			</div>
		</div>
		<div class="content">
			<div class="inner">
				<header class="major">
					<h2>Region-Region ols heatmap</h2>
				</header>
				<p>The coefficients represent the magnitude and direction of the relationship between geographical distribution of disease prevalence per capita and the distribution of research conducted on the disease within specific regions. Observing the diagonal, we can in effect observe that the relationship between prevalence and research is in general not very strong within regions. There are however some relationships in between regions that appear to be stronger. For example, the relationship between prevalence in Western Pacific and research in the Americas seems to be strongly positive. However, we cannot safely make any conclusions from this analysis, as none of the results are statistically significant (p-values are all above 0.10).</p>
			</div>
		</div>
	</section>
</section>
<!-- Three -->
<section id="three">
	<div class="inner">
		<p>What happens if we look at the relationship between the prevalence of a disease in a region and the number of experiments conducted on it in each individual country? The heatmap below shows the results of the linear regression analysis:
		</p>
	</div>
</section>
<section id="two" class="spotlights">
	<section style="display: flex; flex-wrap: wrap; align-items: flex-start;">
		<div style="flex: 2;">
			<div style="width: 450px; height: 338px; overflow: hidden; margin-right: -50px;">
				<iframe 
					src="../assets/geo_analysis_heatmaps/region_country_heatmap.html" 
					style="
					width: 900px; 
					height: 676px;  
					transform: scale(0.5); 
					transform-origin: top left; 
					border: none;
					">
				</iframe>
			</div>
		</div>
		<div class="content">
			<div class="inner">
				<header class="major">
					<h2>Country-Country ols heatmap</h2>
				</header>
				<p>The cells with thick borders indicate statistically significant relationships. We can observe that there are some countries where the relationship between prevalence and research is statistically significant. For example, research in France is positively related to disease prevalence in Africa. In total 15 out of 144 relationships are statistically significant (p-value < 0.1). All these cases represent relationships where the geographical distribution of disease prevalence per capita predicts the distribution of research conducted on the disease within specific countries.</p>
			</div>
		</div>
	</section>
</section>
<!-- Three -->
<section id="three">
	<div class="inner">
		<header class="major">
			<h2>Conclusion</h2>
		</header>
		<p>The analysis shows that there are indeed some relationships between the prevalence of a disease in a region and the amount of research conducted on it in some countries. However, few results are statistically significant. This suggests that the relationship between disease prevalence and research in geographical terms is not very strong, but does exist in some cases. In reality, there are many other factors that can affect the amount of research conducted on a disease, such as the resources available in a country, which probably have a greater impact on the amount of research conducted.
		</p>
	</div>
</section>

</div>

 