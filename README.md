# M2-Generatif

深度生成模型一直是机器学习研究的核心。其重点在于如何对复杂数据分布进行建模和拟合。为了实现这一目标，业界提出了各种深度生成模型，如（VAE）变异自动编码器（Variational Autoencoder）、归一化流（Normalization Flow）、生成对抗网络（GAN）、自回归模型（Autoregressive Model）等。这些模型各有优缺点。

例如，VAE 的最大问题是如何对目标后验分布 △(𝑧|𝑥) 和先验分布 𝑝(𝑧) 进行建模。传统的方法是将这两个分布建模为高斯分布，这样便于采样和计算先验分布与后验分布之间的距离（KL 分歧）。但很明显，VAE 的最大问题在于如何为这两个分布建模：如果设计过于复杂，那么采样和计算 KL 发散就不切实际了。然而，选择虽然简单，却很难表示复杂的数据分布。虽然正则化流程可以精确计算似然函数，但其最大的局限性在于每一步的计算都需要一个可逆函数，这也限制了选择跨度的范围。

GAN 和自回归模型的问题也是显而易见的。GAN 最大的问题是训练特别不稳定，难以适应，容易建模。自回归模型在图像领域的最大问题是生成速度太慢，解码空间太大，难以生成高分辨率图像。

虽然上述问题都可以找到反例，例如，自回归模型可以与 VAE 结合生成高分辨率图像（如 VQGAN），扩散模型可以视为马尔可夫级模型。VAE（MHVAE）和 VAE 可以使用正则化 流建模先验分布等。但上述问题客观存在，也是研究领域的一些主要问题。

Les modèles génératifs profonds ont toujours été au cœur de la recherche sur l’apprentissage automatique. L'accent est mis sur la façon de modéliser et d'ajuster des distributions de données complexes. Afin d'atteindre cet objectif, l'industrie a proposé divers modèles génératifs profonds, tels que les (VAE)Variational Autoencoder, les flux de régularisation Normalization Flow, les réseaux contradictoires génératifs GAN, les modèles autorégressifs (Autoregressive Model), etc. Chacun de ces modèles présente ses propres avantages et inconvénients.

Par exemple, le plus gros problème de VAE est de savoir comment modéliser la distribution a posteriori cible  𝑞(𝑧|𝑥)  et la distribution a priori  𝑝(𝑧) . L'approche traditionnelle consiste à modéliser les deux distributions sous forme de distributions gaussiennes, ce qui est pratique pour échantillonner et calculer la distance entre les distributions antérieure et postérieure (divergence KL). Mais il est évident que le plus gros problème de la VAE est de savoir comment modéliser ces deux distributions : si le plan est trop complexe, il ne sera ni pratique d'échantillonner ni de calculer la divergence KL. Cependant, la sélection est simple mais difficile à représenter une distribution de données complexe. Bien que le flux régularisé permette de calculer la fonction de vraisemblance précise, sa plus grande limitation est que le calcul de chaque étape nécessite une fonction réversible, ce qui limite également la sélection des transformations à chaque étape du flux régularisé, affecte également la capacité globale d’ajustement.

Les problèmes liés au GAN et aux modèles autorégressifs sont également évidents. Le plus gros problème avec GAN est que la formation est particulièrement instable, difficile à adapter et facile à modéliser. Le plus gros problème rencontré par le modèle autorégressif dans le domaine des images est que la vitesse de génération est trop lente et que l'espace de décodage est trop grand, ce qui rend difficile la génération d'images haute résolution.

Bien que on peut trouver des contre-exemples pour chacun des problèmes ci-dessus, par exemple, le modèle autorégressif peut être combiné avec VAE pour générer des images haute résolution (telles que VQGAN), le modèle de diffusion peut être considéré comme un modèle de niveau Markov. VAE (MHVAE) et VAE peuvent utiliser la régularisation Modélisation de flux distribution préalable, etc. Cependant, les problèmes ci-dessus existent objectivement et constituent également quelques-uns des principaux problèmes dans le domaine de la recherche.

