---
title: Drug's Likeness Analysis
layout: post
description: Convey analysis of drug's effectiveness on bonding with the target and select the most "likable" ones.
image: assets/images/likeness.jpg
nav-menu: true
---

<!-- Main -->
<div id="main">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h2>Likeness Analysis</h2>
		</header>
		<p>
            This section explores the drug-likeness of molecules, focusing on their potential to effectively interact with specific biological targets. 
            By applying key criteria like Lipinski's Rule of Five, QED Score, and Veber Criteria, the analysis highlights the essential properties required for successful drug development.
        </p>
        <p>
            These properties include bioavailability, structural flexibility, and the overall suitability of molecules for binding to their targets:
        </p>
        <ul>
            <li>
                <strong>Bioavailability:</strong> Determines how well a drug can be absorbed and reach its target. Factors such as molecular weight, lipophilicity, and hydrogen bonding influence this property.
            </li>
            <li>
                <strong>Structural Flexibility:</strong> Reflected in rotatable bonds, this property affects how easily a molecule can adapt to bind with its target.
            </li>
            <li>
                <strong>Overall Suitability:</strong> Evaluated using polar surface area and QED Score, this ensures molecules maintain a balance between effectiveness and drug-like qualities.
            </li>
        </ul>
        <p>
            Each of the criteria used—Lipinski's Rule of Five, QED Score, and Veber Criteria—contributes to assessing these key properties:
        </p>
        <ul>
            <li>
                <strong>Lipinski's Rule of Five:</strong> Focuses on properties that predict how well a molecule can be absorbed when taken orally, such as size, solubility, and hydrogen bonding.
            </li>
            <li>
                <strong>QED Score (Quantitative Estimate of Drug-likeness):</strong> Combines several factors into a single score to measure the overall balance of a molecule’s properties, ensuring it has the right traits to function effectively as a drug.
            </li>
            <li>
                <strong>Veber Criteria:</strong> Looks at flexibility and surface area to determine if a molecule can move through the body and reach its target efficiently.
            </li>
        </ul>
        <p>
            Together, these criteria and properties guide the identification of the most promising candidates for further research and development.
        </p>
		<p>
            To identify the most likable drugs based on their potential to interact effectively with biological targets, drugs were selected if they meet Lipinski’s Rule and Veber Criteria, and achieve a QED Score in the top 10% (90th percentile). 
        </p> 
	</div>
</section>

<section id="one" class="spotlights" style="padding: 20px;">
    <div style="display: flex; flex-wrap: wrap; align-items: center; justify-content: space-between; max-width: 1200px; margin: 0 auto;">
        <!-- Text Content on the Left -->
        <div class="content" style="flex: 1; min-width: 300px; padding-right: 20px;">
            <div class="inner" style="padding-left: 20px;"> <!-- Added padding to the text -->
                <header class="major">
                    <h3>Criteria Passing Rates</h3>
                </header>
                <p>
                    This bar chart shows the percentage of drugs that meet each criterion on its own, as well as those that pass all three together. It helps to visualize how the criteria overlap and highlights how combining them narrows down the most promising drug candidates. <br> <br> Futher analysis will be based only on the most likable drugs.
				</p>
            </div>
        </div>

        <!-- Chart on the Right -->
        <div style="flex: 1; text-align: center;">
            <iframe src="../assets/plots/Criteria_Passing_Rates.html" width="95%" height="600" frameborder="0"></iframe>
        </div>
    </div>
</section>


<!-- Two -->
<section id="two" class="spotlights">
	<section style="display: flex; flex-wrap: wrap; align-items: flex-start;">
		<div style="flex: 2; margin-right: 20px;">
			<iframe src="../assets/plots/Bubble_Plot.html" width="105%" height="450" frameborder="0"></iframe>
		</div>
		<div class="content" style="flex: 1; min-width: 300px;">
			<div class="inner">
				<header class="major">
					<h3>Molecular Weight vs QED Score</h3>
				</header>
				<p>
		<body>
    <ul>
        <li>
            The clustering of large bubbles within the range below 2000 Daltons (Da) highlights the strong drug-likeness of smaller molecules.
        </li>
        <li>
            As Molecular Weight increases beyond 2000 Da, QED Scores drop significantly, with fewer drug-like molecules observed.
        </li>
        <li>
            Molecules with very high weights, especially above 6000 Da, show almost no drug-like properties.
        </li>
    </ul>
</body></p>
			</div>
		</div>
	</section>
	<section style="display: flex; flex-wrap: wrap; align-items: flex-start;">
		<div style="flex: 2; margin-right: 20px;">
			<iframe src="../assets/plots/Correlation_Heatmap.html" width="100%" height="600" frameborder="0"></iframe>
		</div>
		<div class="content" style="flex: 1; min-width: 300px;">
			<div class="inner">
				<header class="major">
					<h3>Key Insights from the Heatmap</h3>
				</header>
				<p>
				<body>
    <ul>
        <li>
            <strong>Molecular Weight, PSA, and Rotatable Bonds:</strong> 
            These properties are strongly positively correlated, meaning larger molecules tend to have more rotatable bonds and higher polar surface area.
        </li>
        <li>
            <strong>Log P (Lipophilicity):</strong> 
            Negatively correlated with properties like PSA and hydrogen donors/acceptors, indicating that more lipophilic drugs tend to have fewer polar or hydrogen bonding features.
        </li>
        <li>
            <strong>QED Score (Drug-Likeness):</strong> 
            Negatively correlated with Molecular Weight, PSA, and Rotatable Bonds. This implies that highly drug-like compounds are generally smaller, less polar, and more rigid.
        </li>
    </ul>
</body>
</p>
			</div>
		</div>
	</section>
	<section style="display: flex; flex-wrap: wrap; align-items: flex-start;">
		<div style="flex: 2; margin-right: 20px;">
			<img src="../assets/plots/Correlation_Heatmap.html" alt="" data-position="25% 25%" style="width: 100%; height: auto;" />
		</div>
		<div class="content" style="flex: 1; min-width: 300px;">
			<div class="inner">
				<header class="major">
					<h3>Sed nunc ligula</h3>
				</header>
				<p>Nullam et orci eu lorem consequat tincidunt vivamus et sagittis magna sed nunc rhoncus condimentum sem. In efficitur ligula tate urna. Maecenas massa sed magna lacinia magna pellentesque lorem ipsum dolor. Nullam et orci eu lorem consequat tincidunt. Vivamus et sagittis tempus.</p>
				<ul class="actions">
					<li><a href="generic.html" class="button">Learn more</a></li>
				</ul>
			</div>
		</div>
	</section>
</section>

<!-- Three -->
<section id="three">
	<div class="inner">
		<header class="major">
			<h2>Massa libero</h2>
		</header>
		<p>Nullam et orci eu lorem consequat tincidunt vivamus et sagittis libero. Mauris aliquet magna magna sed nunc rhoncus pharetra. Pellentesque condimentum sem. In efficitur ligula tate urna. Maecenas laoreet massa vel lacinia pellentesque lorem ipsum dolor. Nullam et orci eu lorem consequat tincidunt. Vivamus et sagittis libero. Mauris aliquet magna magna sed nunc rhoncus amet pharetra et feugiat tempus.</p>
		<ul class="actions">
			<li><a href="generic.html" class="button next">Get Started</a></li>
		</ul>
	</div>
</section>

</div>
