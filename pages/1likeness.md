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
			<h2>Which molecules have a potencial for further research?</h2>
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
	</div>
</section>

<section id="one" class="spotlights" style="padding: 20px;">
    <div style="display: flex; flex-wrap: wrap; align-items: center; justify-content: space-between; max-width: 1400px; margin: 0 auto;">
        <!-- Chart on the Left -->
        <div style="flex: 1; text-align: center; max-width: 60%;">
            <iframe src="../assets/plots/Distribution_qed.html" width="100%" height="600" frameborder="0"></iframe>
        </div>

        <!-- Text Content on the Right -->
        <div class="content" style="flex: 1; min-width: 300px; padding-left: 40px; max-width: 40%;">
            <div class="inner" style="padding-right: 20px;"> <!-- Added padding to the text -->
                <header class="major">
                    <h3>How the most likable drugs will be identified?</h3>
                </header>
                <p>
                    To identify the most likable drugs based on their potential to interact effectively with biological targets, drugs were selected if they meet Lipinski’s Rule and Veber Criteria, and achieve a QED Score in the top 10% (90th percentile). 
                </p>
            </div>
        </div>
    </div>
</section>


<section id="one" class="spotlights" style="padding: 20px;">
    <div style="display: flex; flex-wrap: wrap; align-items: center; justify-content: space-between; max-width: 1400px; margin: 0 auto;">
        <!-- Text Content on the Left -->
        <div class="content" style="flex: 1; min-width: 300px; max-width: 40%; padding-right: 20px;">
            <div class="inner" style="padding-left: 20px;"> <!-- Added padding to the text -->
                <header class="major">
                    <h3>Criteria Passing Rates</h3>
                </header>
                <p>
                    The bar chart shows that the majority of drugs pass only the Veber Criteria (25.1%), while a smaller percentage (9.9%) meet all three criteria. Few drugs meet only Lipinski’s Rule (2.7%) or QED Score requirements alone (0.1%), highlighting the stringency of combining all criteria.
				</p>
            </div>
        </div>

        <!-- Chart on the Right -->
        <div style="flex: 2; text-align: center; max-width: 60%;">
            <iframe src="../assets/plots/Criteria_Passing_Rates.html" width="100%" height="600" frameborder="0"></iframe>
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
            The clustering of large bubbles within the range below 2000 Daltons (Da) highlights <span style="color:rgb(0, 142, 81);">the strong drug-likeness of smaller molecules</span>.
        </li>
        <li>
            As Molecular Weight increases beyond 2000 Da, QED Scores drop significantly, with fewer drug-like molecules observed.
        </li>
        <li>
            <span style="color: #D3AF36;">Molecules with very high weights</span>, especially above 6000 Da, <span style="color: #D3AF36;">show almost no drug-like properties</span>.
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

<!-- Three -->
<section id="three" style="padding: 40px 20px;">
    <div class="inner" style="padding: 0 40px;">
        <header class="major">
            <h2>Conclusion</h2>
        </header>
        <p>
            This analysis provides valuable insights into identifying promising drug candidates by evaluating key properties such as bioavailability, flexibility, and overall suitability for biological targets. Using criteria like Lipinski’s Rule of Five, Veber Criteria, and QED Score, the study highlights important factors that make a molecule more “drug-like.”
            <br><br>
            <span style="color:rgb(0, 142, 81);">Smaller molecules, with lower molecular weights, tend to score higher on drug-likeness</span>, showing better bioavailability and suitability. Larger molecules, on the other hand, often struggle to meet these criteria, <span style="color:rgb(179, 35, 162);">making molecular weight a critical factor in drug development</span>. The heatmap reveals a strong positive correlation between molecular weight and rotatable bonds, indicating that <span style="color: #D3AF36;">larger molecules tend to have greater structural flexibility</span>. This flexibility can influence how well a molecule interacts with its target, balancing binding potential and drug-like behavior.
            <br><br>
            By combining these tools, the analysis identifies the most promising molecules for further research. This process helps narrow down the options, making drug discovery more efficient and focused.
        </p>
    </div>
</section>
