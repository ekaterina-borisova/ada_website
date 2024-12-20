---
title: Drug-Drug Interaction Analysis & Prediction
layout: post
description: 'Analyse Drug-Drug pair for the severity of their antagonistic interaction and define predictive model'
image: assets/images/ddi.png
nav-menu: true
---

<!-- Main -->
<div id="main">


<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h2>Can one predict interaction of two newly developed drugs?</h2>
		</header>
		<p>Testing drugs on their compatibility is one of the major issues in nowadays pharmacology, as these interactions can significantly impact drug efficacy and patient safety. By leveraging data from DrugBank on examples of synergetic drug-drug interactions we came up with several models on how to predict newly developed drugs' interactions. This research combines natural language processing, clustering, and machine learning to tackle the complexities of DDI analysis. By embedding interaction descriptions using BioBERT, we created rich, context-aware representations for clustering interactions based on severity. Furthermore we look at possible interesting finding related to severity of interaction in "likable" drugs. Finally by encoding SMILES of each drug, we use Neural-Network models to predict a potential severity of synergetic interactions. This comprehensive approach aims to enhance our understanding of DDIs and contribute to safer, more effective pharmacological practices.</p>
	</div>
</section>

<!-- Two -->
<section id="two" class="spotlights">
    <section>
        <div style="flex: 2; display: flex; justify-content: center; align-items: center;">
            <img src="{% link assets/images/BioBert.png %}" alt="BioBert" width="100%" frameborder="0"/>
        </div>
        <div class="content" style="flex: 1;">
            <div class="inner">
                <header class="major">
                    <h3>BioBert & Clustering Interactions</h3>
                </header>
                <p>BioBERT (Bidirectional Encoder Representations from Transformers for Biomedical Text Mining) is a domain-specific extension of the BERT language model, designed specifically for biomedical and clinical text. Unlike standard BERT, which is trained on general language data, BioBERT incorporates large-scale biomedical corpora such as PubMed and PMC articles.</p>
            </div>
        </div>
    </section>
    <section>
        <div style="flex: 2; display: flex; justify-content: center; align-items: center;">
            <iframe src="../assets/plots/label_bar_chart.html" width="100%" height="500" frameborder="0"></iframe>
        </div>
        <div class="content" style="flex: 1;">
            <div class="inner">
                <p>Once we utilized BioBERT to generate embeddings for each drug-drug interaction (DDI) description, we applied the K-Means algorithm to cluster the interactions based on the severity of their effects. The interactions were grouped into three main categories: <span style="color:rgb(0, 142, 81);">Minor</span>, <span style="color: #D3AF36;">Moderate</span>, and <span style="color:rgb(179, 35, 162);">Major</span>. Notably, a greater number of DDIs were classified as <span style="color: #D3AF36;">Moderate</span>, reflecting a prevalent level of intermediate severity in the dataset.</p>
            </div>
        </div>
    </section>
</section>

<!-- One -->
<section id="one">
	<div class="inner">
		<p>To further understand the characteristics of the clustered interactions, we analyzed the text descriptions within each severity category. Word clouds were generated to visualize the most frequent terms associated with ‘Minor,’ ‘Moderate,’ and ‘Major’ interactions, offering a quick insight into the dominant themes and keywords in each group.</p>
	</div>
</section>

<section id="two" class="spotlights">
	<section>
		<iframe src="../assets/plots/wordcloud_dropdown.html" width="100%" height="500" frameborder="0"></iframe>
	</section>
	<section>
		<a href="generic.html" class="image">
			<div class="hover-image-wrapper">
				<img src="{% link assets/images/mol.png %}" alt="" class="image-default" />
				<img src="{% link assets/images/fingerprints.png %}" alt="" class="image-hover" />
			</div>
		</a>
		<div class="content">
			<div class="inner">
				<header class="major">
					<h3>Fingerprint Transformation using RDKit</h3>
				</header>
				<p>Our prediction model is based on SMILES structure of two drugs, thus we first need to encode those molecular structures. For this purpose we used Morgan fingerprints transformation provided by RDKit that converts SMILES into 1024-bits vector encoding. These fingerprints allow to encode the presence or absence of specific molecular substructures or patterns that might be crusial in the prediction of their interaction. By applying this numerical transformations it allows molecules to be efficiently compared or used in predictive models.</p>
			</div>
		</div>
	</section>
	<section>
		<div style="flex: 2; display: flex; justify-content: center; align-items: center;">
            <iframe src="../assets/plots/nn_cm.html" width="100%" height="500" frameborder="0"></iframe>
        </div>
		<div class="content">
			<div class="inner">
				<header class="major">
					<h3>Prediction Model</h3>
				</header>
				<p>By taking Morgan fingerprints of two drugs as the input, we are capable of developing a model that could predict the interaction between drug pairs. We use Neural-Network approach to solve this problem. First the NN model treats each drug separately but after two sequential layers, it merges the two inputs in order to make a final prediction. Our model achieves a <b>97.48%</b> overall accuracy in its prediction.</p>
				<ul class="actions">
					<li><a href="{{ site.baseurl }}/pages/nn.html" class="button">Learn more</a></li>
				</ul>
			</div>
		</div>
	</section>
	<section>
        <div style="flex: 2; display: flex; justify-content: center; align-items: center;">
            <iframe src="../assets/plots/label_bar_chart_with_ddi_frequencies.html" width="100%" height="500" frameborder="0"></iframe>
        </div>
        <div class="content" style="flex: 1;">
            <div class="inner">
				<header class="major">
					<h3>DDI of "Likable" Drugs</h3>
				</header>
                <p>Our initial hypothesis suggested that “likable” drugs would have less severe interactions with other drugs. To test this, we examined the severity of interactions where at least one drug was considered “likable.” However, the results indicate that the likability of a drug does not significantly impact the severity of its interactions with other drugs. As a result, we can reject our hypothesis. Based on these findings, we believe that the most effective model for prediction is one that focuses solely on the molecular structures of each drug.</p>
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
		<p>In this study, we explored various approaches to predict the interactions between newly developed drugs using data from DrugBank. We utilized BioBERT for embedding drug-drug interaction (DDI) descriptions, followed by clustering based on interaction severity, revealing that moderate interactions were most prevalent. Additionally, we employed SMILES-based molecular structures encoded as Morgan fingerprints and used a Neural Network model to predict the severity of drug interactions, achieving a high accuracy of 97.48%. Our hypothesis that “likable” drugs would have less severe interactions was not supported by the data, leading us to conclude that molecular structure-based models are more effective. This research provides valuable insights into DDI prediction and highlights the potential of molecular structure analysis for more accurate predictions.</p>
	</div>
</section>

</div>


<style>
    .hover-image-wrapper {
        position: relative;
        width: 100%;
        height: 100%;
        display: block;
        overflow: hidden;
    }

    .hover-image-wrapper img {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: opacity 0.3s ease;
    }

    .hover-image-wrapper .image-hover {
        opacity: 0;
    }

    .hover-image-wrapper:hover .image-default {
        opacity: 0;
    }

    .hover-image-wrapper:hover .image-hover {
        opacity: 1;
    }
	
</style>