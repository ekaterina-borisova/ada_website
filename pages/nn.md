---
layout: post
title: Neural-Nework Model
description: Prediction model for DDI
image: assets/images/nn.png
nav-menu: false
---
<div class="row">
    <div class="6u 12u$(small)">
        <h4>Model Definition</h4>
        <ul class="alt">
            <li>Input: Two drug fingerprints, each of size 1024.</li>
            <li>Encoder: Two-layer fully connected neural network with ReLU activation.</li>
            <li>Classifier: Merges encoded fingerprints and predicts interaction severity class (3 classes).</li>
            <li>Data-split: Stratified split on 80% - train, 10% - validation, 10% - test</li>
            <li>Training Epochs: 100 unless reached convergence in validation accuracy</li>
            <li>Learning Rate: 0.001</li>
            <li>Batch Size: 2048</li>
        </ul>
</div>

<div style="text-align: center;">
    <img src="{{ site.url }}{{ site.baseurl }}/assets/images/nn.png" alt="" data-position="25% 25%" />
</div>
