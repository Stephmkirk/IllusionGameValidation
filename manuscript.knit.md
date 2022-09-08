---
title             : "**The Illusion Game: A Novel Experimental Paradigm Provides Evidence in Favour of a General Factor of Visual Illusion Sensitivity and Personality Correlates**"
shorttitle        : "Illusion Game Validation"
author:
  - name          : "Dominique Makowski"
    affiliation   : "1"
    corresponding : yes    # Define only one corresponding author
    address       : "HSS 04-18, 48 Nanyang Avenue, Singapore"
    email         : "dom.makowski@gmail.com"
    orcid         : 0000-0001-5375-9967
    role:         # Contributorship roles (e.g., CRediT, https://casrai.org/credit/)
      - "Conceptualization"
      - "Data curation"
      - "Formal Analysis"
      - "Funding acquisition"
      - "Investigation"
      - "Methodology"
      - "Project administration"
      - "Resources"
      - "Software"
      - "Supervision"
      - "Validation"
      - "Visualization"
      - "Writing – original draft"
  - name          : "An Shu Te"
    affiliation   : "1"
    orcid         : 0000-0001-8008-2824
    role:
      - "Project administration"
      - "Resources"
      - "Investigation"
      - "Writing – original draft"
  - name          : "Stephanie Kirk"
    affiliation   : "1"
    orcid         : 0000-0002-9312-5552
    role:
      - "Project administration"
      - "Resources"
      - "Writing – original draft"
  - name          : "Ngoi Zi Liang"
    affiliation   : "1"
    role:
      - "Project administration"
      - "Resources"
      - "Writing – review & editing"
  - name          : "S.H. Annabel Chen"
    affiliation   : "1, 2, 3, 4"
    orcid         : 0000-0002-1540-5516
    role:
      - "Project administration"
      - "Supervision"
      - "Writing – review & editing"
      
affiliation:
  - id            : "1"
    institution   : "School of Social Sciences, Nanyang Technological University, Singapore"
  - id            : "2"
    institution   : "LKC Medicine, Nanyang Technological University, Singapore"
  - id            : "3"
    institution   : "National Institute of Education, Singapore"
  - id            : "4"
    institution   : "Centre for Research and Development in Learning, Nanyang Technological University, Singapore"
    
authornote: |
  Correspondence concerning this article should be addressed to Dominique Makowski, HSS 04-18, 48 Nanyang Avenue, Singapore (dom.makowski@gmail.com).
abstract: |
  Visual illusions highlight how the brain uses contextual and prior information to inform our perception of reality. Unfortunately, illusion research has been hampered by the difficulty of adapting these stimuli to experimental settings. In this set of studies, we used the parametric framework for visual illusions implemented in the *Pyllusion* software to generate 10 different classic illusions (Delboeuf, Ebbinghaus, Rod and Frame, Vertical-Horizontal, Zöllner, White, Müller-Lyer, Ponzo, Poggendorff, Contrast) varying in strength. We tested the objective effect of the illusions on errors and reaction times in a perceptual discrimination task, from which we extracted participant-level performance scores (n=250). Our results provide evidence in favour of the existence of a general factor (labelled Factor *i*) underlying the sensitivity to different illusions. Moreover, we report a positive relationship between illusion sensitivity and personality traits such as Agreeableness, Honesty-Humility, and negative relationships with Psychoticism, Antagonism, Disinhibition, and Negative Affect.

keywords          : "visual illusions, illusion game, Pyllusion, personality, general factor"
wordcount         : "5099"
bibliography      : references.bib
floatsintext      : yes
linenumbers       : yes
draft             : no
mask              : no
figurelist        : yes
tablelist         : no
footnotelist      : no
classoption       : "man"
output            : papaja::apa6_pdf
csl: utils/apa.csl
header-includes:
  - \usepackage[labelfont=bf, font={scriptsize, color=gray}]{caption}
editor_options:
  chunk_output_type: console
---



<!-- Significance Statement (< 120 words) -->
<!-- A novel paradigm to study the objective effect of visual illusions is presented, which yielded evidence in favor of a common factor to visual illusions (Factor *i*) and a relationship between a low illusion sensitivity and maladaptive personality traits, such as antagonism, psychoticism and disinhibition. -->

# Introduction

<!-- Intro  & Gaps-->

Visual illusions are fascinating stimuli capturing a key feature of our neurocognitive systems. They eloquently show that our brains did not evolve to be perfect perceptual devices providing veridical accounts of physical reality, but integrate prior knowledge and contextual information - blended together in our subjective conscious experience [@carbon2014]. Despite the longstanding interest within the fields of visual perception [@day1972; @eagleman2001; @gomez-villa2022], consciousness science [@caporuscio2022; @lamme2020], and psychiatry [@notredame2014; @gori2016; @razeghi2022; @teufel2015], several important issues remain open.

Notably, the presence of a common mechanism underlying the effect of different illusions has been contested [@hamburger2016; @cretenoud2019; @cretenoud2020illusions]; and the nature of the underlying processes - whether related to low-level features of the visual processing system [@cretenoud2019; @gori2016] or to top-down influences of prior beliefs [@teufel2018; @caporuscio2022] are strongly debated. The existence of dispositional correlates of illusion sensitivity is another area of controversy, with some studies reporting higher illusion resistance in patients with schizophrenia and autism [@notredame2014; @park2022; @giaouri2011; @keane2014; @pessoa2008] and in individuals with stronger aggression and narcissism traits [@zhang2017; @konrath2009seeing].

<!-- Pyllusion -->

One key challenge hindering the further development of illusion research is the relative difficulty of adapting visual illusions to an experimental setting, which typically requires the controlled modulation of the specific variables of interest. To address this issue, we first developed a parametric framework to manipulate visual illusions, which we implemented and made accessible in the open-source software *Pyllusion* [@makowski2021]. This software allows us to generate different types of classic visual illusions with a continuous and independent modulation of two parameters: *illusion strength* and *task difficulty* (see **Figure 1**).

\begin{figure}
\includegraphics[width=1\linewidth]{figures/Figure1} \caption{The parametric framework for visual illusions (Makowski et al., 2021) applied to the Müller-Lyer illusion (above). Below are examples of stimuli showcasing the manipulation of two parameters, task difficulty and illusion strength.}(\#fig:unnamed-chunk-2)
\end{figure}

<!-- Target, strength, difficulty -->

Indeed, many visual illusions can be seen as being composed of *targets* (e.g., same-length lines), of which perception is biased by the *context* (e.g., in the Müller-Lyer illusion, the same-length line segments appear to have different lengths when they end with inwards or outwards pointing arrows). Past illusion studies traditionally employed paradigms focusing on participants' subjective experience, by asking them the extent to which they perceive two identical targets as different [@lanyi2022can], or having them adjust the targets to match a reference stimulus relying only on their perception [@mylniec2016; @grzeczkowski2018]. Alternatively, *Pyllusion* allows the creation of illusions in which the targets are objectively different (e.g., one segment is truly more or less longer than the other), and in which the illusion varies in strength (the biasing angle of the arrows is more or less acute).

<!-- Paradigm -->

This opens the door for an experimental task in which participants make perceptual judgments about the targets (e.g., which segment is the longest) under different conditions of objective difficulty and illusion strength. Moreover, the illusion effect can be either "incongruent" (making the task more difficult by biasing the perception in the opposite way) or "congruent" (making the task easier). Although visual illusions are inherently tied to subjective perception, this framework allows a reversal of the traditional paradigm to potentially quantify the "objective" effect of illusions by measuring its behavioral effect (error rate and reaction times) on the performance in a perceptual task.

<!-- Goals -->

In the present set of preregistered studies, we will first test this novel paradigm by investigating if the effect of illusion strength and task difficulty can be manipulated continuously, and separately modeled statistically. Then, we will further utilize the paradigm to assess whether 10 different classic illusions (Delboeuf, Ebbinghaus, Rod and Frame, Vertical-Horizontal, Zöllner, White, Müller-Lyer, Ponzo, Poggendorff, Contrast) share a common latent factor. Finally, we will investigate how the the inter-individual sensitivity to illusions relates to dispositional variables, such as demographic characteristics and personality.

In line with open-science standards, all the material (stimuli generation code, experiment code, raw data, analysis script with complementary figures and analyses, preregistration, etc.) is available at [**https://github.com/RealityBending/IllusionGameValidation**](https://github.com/RealityBending/IllusionGameValidation){.uri}.

# Study 1

## Aim

Study 1 can be seen as a pilot experiment aiming to gather some preliminary data to assess if the stimuli generated by *Pyllusion* behaves as expected for each of the 10 illusion types (i.e., whether an increase of task difficulty and illusion strength leads to an increase of errors), and develop an intuition about the magnitude of effects, to refine the stimuli parameters to a more sensible range (i.e., not overly easy and not impossibly hard) for the next study.

## Procedure

We generated 56 stimuli for each of the 10 illusion types. These stimuli resulted from the combination of 8 linearly-spread levels of task difficulty (e.g., [1, 2, 3, 4, 5, 6, 7], where 1 corresponds to the highest difficulty - i.e., the smallest objective difference between targets) and 7 levels of illusion strength (3 values of strength on the congruent side, 3 on the incongruent side, and 0; e.g., [-3, -2, -1, 0, 1, 2, 3], where negative values correspond to congruent illusion strengths).

The 10 illusion blocks were randomly presented, and the order of the 56 stimuli within the blocks was also randomized. After the first series of 10 blocks, another series was administered (with new randomized orders of blocks and trials). In total, each participant saw 56 different trials per 10 illusion type, repeated 2 times (total = 1120 trials), to which they had to respond "as fast as possible without making errors" (i.e., an explicit double constraint to mitigate the inter-individual variability in the speed-accuracy trade off). The task was implemented using *jsPsych* [@de2015jspsych], and the instructions for each illusion type are available in the experiment code.

## Participants

Fifty-two participants were recruited via *Prolific* ([www.prolificacademic.co.uk](www.prolificacademic.co.uk)), a crowd-sourcing platform providing high data quality [@peer2022]. The only inclusion criterion was a fluent proficiency in English to ensure that the task instructions would be well-understood. Participants were incentivised with a reward of about \textsterling 7.5 for completing the task, which took about 50 minutes to finish.

We removed 6 participants upon inspection of the average error rate (when close to 50%, suggesting random answers), and when the reaction time distribution was implausibly fast. For the remaining participants, we discarded blocks where the error rate was higher than 50% (possibly indicating that instructions got misunderstood; e.g., participants were selecting the shorter line instead of the longer one). Finally, we removed 692 (1.37%) trials based on an implausibly short or long response time (\< 150 ms or \> 3000 ms).

The final sample included 46 participants (Mean age = 26.7, SD = 7.7, range: [19, 60]; Sex: 39.1% females, 56.5% males, and 4.4% other).

## Data Analysis

The analysis of study 1 focused on the probability of errors as the main outcome variable. For each illusion, we started by visualizing the average effect of task difficulty and illusion strength to gain some intuition on the underlying generative model. Next, we tested the performance of various logistic models differing in their specifications, such as: with or without a transformation of the task difficulty (log, square root or cubic root), with or without a 2nd order polynomial term for the illusion strength, and with or without the illusion side (up *vs.* down or left *vs.* right) as an additional predictor. We then fitted the best performing model under a Bayesian framework, and compared its visualization with that of a General Additive Model (GAM), which has an increased ability of mapping underlying potential non-linear relationships (at the expense of model simplicity).

The analysis was carried out using *R 4.2* [@RCoreTeam2022], *brms* [@Burkner2017], the *tidyverse* [@wickham2019], and the *easystats* collection of packages [@bayestestRArticle; @correlationArticle; @performanceArticle; @insightArticle].

## Results

The statistical models suggested that the effect of task difficulty had a cubic relationship with error rate for the Delboeuf and Ebbinghaus illusions (both composed of circular shapes), square relationship for the Rod and Frame and Vertical-Horizontal illusions, cubic relationship for the Zöllner and Poggendorff illusions, exponential relationship for the White illusion, cubic relationship for the Müller-Lyer and Ponzo illusions (both based on line lengths), and linear relationship for the Contrast illusion. All models suggested a significant effect of illusion strength and task difficulty. See details and figures in the analysis script.

## Discussion

This study provided a clearer understanding of the magnitude of the parametric effects at stake and the type of interaction between them. Furthermore, it allowed us to better understand and test the stimuli generated by *Pyllusion*, as well as uncover incidental bugs and technical issues (for instance, the specification direction of the illusion strength was reversed for a few illusions), which were fixed in a new software release. Crucially, this study allowed us to refine the range of task difficulty and illusion strength values in order to maximize information gain.

In most illusions, the task difficulty exhibited monotonic power-law scaled effects, which is in line with the psychophysics literature on perceptual decisions [@ditzinger2010; @shekhar2021; @bogacz2006]. One notable result was the illusion effect pattern for the Zöllner illusion, which suggested a non-linear relationship. By generating a wider range of illusion strength values, the next study will attempt at clarifying this point.

# Study 2

## Aim

The aim of study 2 was two-fold. In the first part, we carefully modeled the error rate and the reaction time of each illusion type in order to validate our novel paradigm and show that the effect of illusions can be manipulated continuously. In the second part, we derived the participant-level scores from the models (i.e., the effect of illusion strength for each individual) and analyzed their latent factors structure.

## Procedure

The paradigm of study 2 was similar to that of study 1, with the following changes: the illusory stimuli were re-generated within a refined space of parameters based on the results of study 1. Moreover, taking into account the findings of study 1, we used non-linearly spaced difficulty levels, depending on the best underlying model (i.e., with an exponential, square or cubic spacing depending on the relationship). For instance, a linear space of [0.1, 0.4, 0.7, 1.0] can be transformed to an exponential space of [0.1, 0.34, 0.64, 1.0].

Additionally, instead of repeating each stimulus two times, we generated illusions using more levels of difficulty and illusion strength. As such, for each illusion type, we generated a total of 134 stimuli that were split into two groups (67 stimuli per illusion block). Furthermore, instead of a simple break screen, we added two personality questionnaires between the two series of 10 illusion blocks (see study 3).

## Participants

Using the same recruitment procedure as in study 1, we recruited 256 participants, out of which 6 were identified as outliers and excluded, leaving a final sample of 250 participants (Mean age = 26.5, SD = 7.6, range: [18, 69]; Sex: 48% females, 52% males). Please see study 3 for the full demographic breakdown. We discarded blocks with more than 50% of errors (2.16% of trials) and 0.76% trials with extreme response times (\< 125 ms or \> 4 SD above mean).

## Data Analysis

The first part of the analysis focused on modelling the effect of illusion strength and task difficulty on errors and reaction time (RT) within each illusion. In order to achieve this, we started by fitting General Additive Models (GAMs), which can accommodate possible non-linear effects and interactions. Errors were analyzed using Bayesian logistic mixed models, and RTs of correct responses were analyzed using an ex-Gaussian family with the same fixed effects entered for the location $\mu$ (mean), scale $\sigma$ (spread) and tail-dominance $\tau$ of the RT distribution [@balota2011moving; @matzke2009psychological].

Using GAMs as the "ground-truth" models, we attempted at approximating them using general linear models, which have the advantage of estimating the participant-level variability of the effects (via random slopes). Following a comparison of models with a combination of transformations (raw, log, square root or cubic root) on the main predictors (task *difficulty* and illusion *strength*), we selected and fitted the best model (based on their indices of fit), and compared their output visually (see **Figure 2**).

We then extracted the inter-individual variability in the effect of illusion strength and its interaction with task difficulty, and used it as participant-level scores. Finally, we explored the relationship of these indices across different illusions using exploratory factor analysis (EFA) and structural equation modelling (SEM).

## Results

The best models were $log(diff)*strength$ for Delboeuf; $sqrt(diff)*strength$ for Ebbinghaus; $log(diff)*log(strength)$ for Rod and Frame; $sqrt(diff)*sqrt(strength)$ for Vertical-Horizontal; $cbrt(diff)*strength$ for Zöllner; $diff*sqrt(strength)$ and $log(diff)*strength$ respectively for errors and RT in White; $sqrt(diff)*sqrt(strength)$ and $sqrt(diff)*strength$ respectively for errors and RT in Müller-Lyer; $cbrt(diff)*strength$ for Ponzo; $cbrt(diff)*sqrt(strength)$ and $cbrt(diff)*strength$ respectively for errors and RT in Poggendorff; and $sqrt(diff)*sqrt(strength)$ for Contrast. For all of these models, the effects of illusion strength, task difficulty and their interaction were significant.

For error rates, most of the models closely matched their GAMs counterpart (see **Figure 2**), with the exception of Delboeuf (for which the GAM suggested a non-monotonic effect of illusion strength with a local minimum at 0) and Zöllner (for which theoretically congruent illusion effects were related to increased error rate).

\begin{figure}
\includegraphics[width=1\linewidth]{figures/Figure2} \caption{Top: the effect of illusion strength and task difficulty on the error rate and reaction time (RT) for each individual illusion. The solid line represents the General Additive Model (GAM), and the dashed line corresponds to its approximation via linear models. Descriptive data is shown with stacked dots (for which errors start from the top) and distributions for RTs. Negative values for illusion strength correspond to congruent (i.e., facilitating) illusion effects. Task difficulty (the objective difference between the targets of perceptual decision) levels are shown as colors, with lower values corresponding to harder trials. The results for each illusion are surrounded by 4 extreme examples of stimuli, corresponding to the hardest difficulty (on top) and the strongest illusion (on the right for incongruent illusions). Bottom: We extracted the effect slope of the illusion strength and its interaction with task difficulty for each participant. We fitted a Structural Equation Model (SEM) suggesting that these manifest variables group to first-level illusion-specific latent factors, which then load on a general factor of illusion sensitivity (Factor \textit{i}).}(\#fig:unnamed-chunk-3)
\end{figure}

For RTs, the GAMs suggested a consistent non-linear relationship between RT and illusion strength: as the illusion strength increases beyond a certain threshold, the participants respond faster. While this is is not surprising (strong illusions are likely so effective in biasing perception that it is "easier", i.e., faster, to make the wrong decision), the linear models were not designed to capture this - likely quadratic - pattern and hence are not good representatives of the underlying dynamics. As such, we decided not to use them for the individual scores analysis. <!-- Additionally, it would have increased the parameter space from 20 to 40 variables, which was deemed as statistically unreasonable given our sample size). -->

Though imperfect, we believe that the random-slope models capture inter-individual differences with more accuracy (and are also more conservative estimates due to shrinkage) than basic empirical scores, such as the total number of errors, or the average RT. Thus, for each illusion and within each participant, we extracted the effect of illusion strength and its interaction with task difficulty when the illusion effect was incongruent. These twenty participant-level scores were subjected to exploratory factor analysis (EFA). The Method Agreement Procedure [@parametersArticle] suggested the presence of 7 latent factors. An oblique (*oblimin* rotation) factor solution explaining 66.69% of variance suggested separate dimensions for the effect of Zöllner, White, Poggendorff, Contrast, Ebbinghaus, Delboeuf, and a common factor for the parameters related to Müller-Lyer, Vertical-Horizontal, Ponzo and Rod and Frame. We submitted these factors to a second-level analysis and extracted two orthogonal (*varimax* rotation) factors. The first factor was loaded by all the previous dimensions with the exception of Delboeuf, which formed its own separate factor.

Finally, we tested this data-driven model (*m0*) against four other structural models using structural equation modelling (SEM): one in which the two parameters of each of the 10 illusions (illusion strength and interaction with task difficulty) loaded on separate factors, which then all loaded on a common factor (*m1*); one in which the parameters were grouped by illusion type (lines, circles, contrast and angle) before loading on a common factor (*m2*); one in which all the parameters related to strength, and all the parameters related to the interaction loaded onto two respective factors, which then loaded on a common factor (*m3*); and one in which there was no intermediate level: all 20 parameters loaded directly on a common factor (*m4*).

The model *m1*, in which the parameters loaded on a first level of 10 illusion-specific factors, which then all loaded on a common factor, significantly outperformed the other models. Its indices of fit ranged from acceptable to satisfactory (CFI = .92; SRMR = .08; NNFI = .91; PNFI = .74; RMSEA = .08), and all the specified effects were significant. The illusion-specific latent factors were loaded positively by the sensitivity to illusion strength, as well as by the interaction effect with task difficulty (with the exception of Delboeuf, Ebbinghaus, Vertical-Horizontal, Müller-Lyer and Contrast, for which the loading was negative). The general factor of illusion sensitivity, labelled Factor *i* (i- for illusion), explained 48.02% of the total variance of the initial dataset, and was strongly related to Vertical-Horizontal ($\beta_{std.}=0.83$), Müller-Lyer ($\beta_{std.}=0.76$), Ponzo ($\beta_{std.}=0.65$), Ebbinghaus ($\beta_{std.}=0.64$); moderately to Zöllner ($\beta_{std.}=0.53$), Poggendorff ($\beta_{std.}=0.44$), Rod and Frame ($\beta_{std.}=0.42$), Contrast ($\beta_{std.}=0.40$) and White ($\beta_{std.}=0.35$); and weakly to Delboeuf ($\beta_{std.}=0.19$). We then computed, for each participant, the score for the 10 illusion-specific factors and for the general Factor *i*.

It is important to note that these individual scores are the result of several layers of simplification: 1) the individual coefficient is that of simpler models that sometimes do not perfectly capture the underlying dynamics (especially in the case of Delboeuf and Zöllner); 2) we only used the models on error rate, which could be biased by the speed-accuracy decision criterion used by participants; 3) the structural equation model used to compute the scores also incorporated multiple levels of abstractions. Thus, in order to validate the individual scores, we computed the correlation between them and simple empirical scores, such as the average error rate and the mean RT in the task. This analysis revealed strong and significant correlations between each illusion-specific factor and the average amount of errors in its corresponding task. Moreover, each individual score was strongly associated with the average RT across multiple illusion types. This suggests that the individual scores obtained from the structural equation model do capture the sensitivity of each participant to visual illusions, manifesting in both the number of errors and long reaction times.

## Discussion

This study confirmed that it was possible to continuously manipulate the effect of illusion strength for 10 classic illusions. Increasing the illusion strength increased the likelihood of errors, as well as the average and spread of RTs (but only up to a point, after which participants become faster at responding with the wrong answer). Future studies are needed to explore reaction times and identify the most appropriate models, and/or use models that integrate both errors and reaction time (e.g., drift diffusion models).

The effect on errors was monotonic for most illusions, with the exception of Delboeuf and Zöllner. For both of them, mildly congruent illusion strengths (which theoretically were supposed to be associated with fewer errors than incongruent effects) were related to small and strong increases of errors, respectively. For the Delboeuf illusion, we believe that this was due to an artifact caused by the illusion generation algorithm: the outline of the target circles was always created as slightly bigger, which made the difference between them more obvious at an illusion strength of 0. This was fixed in the latest release of *Pyllusion* (v1.2), which now generates outlines of the same size as the target circle. For the Zöllner illusion, the observed non-monotonic pattern is actually consistent with previous reports [@kitaoka2000; @kitaoka2007], suggesting an acute angle contraction effect at very small - as well as at sufficiently large angles (below 10 degrees for the former and between 50 to 90 degrees for the latter) between the target horizontal line and the biasing horizontal bars when the illusion strength is weak.

Finally, this study provided evidence for both the existence of illusion-specific factors, as well as for a common latent factor (labelled Factor *i*) that explained about half of the total variance. These participant-level scores were positively related to the error rate and average reaction time, and can thus be interpreted as indices of illusion sensitivity.

# Study 3

## Aim

Study 3 aimed at investigating the links between the inter-individual scores of illusion sensitivity (obtained in study 2), contextual variables (pertaining to the experiment setting), such as screen size, demographic features (such as sex and age), and stable dispositional variables such as "general" personality traits. Indeed, despite the abundant literature on visual illusions, relatively few studies have investigated its ties with participants' characteristics. Research examining the influence of demographic variables such as gender and age have generally found inconsistent results [@cretenoud2020individual; @grzeczkowski2017; @lo2011; @papageorgiou2020]. Regarding links with personality, most works focused on traits associated with psychopathology, such as impulsivity or sensation-seeking [@hlavata2018; @zhang2017; @lanyi2022can; @pessoa2008].

## Procedure

This study was based on the data collected in study 2. The variables of interest here were taken from the questionnaires that were inserted in between the two series of illusion blocks. We used the *IPIP6* [24 items, @sibley2011] to measure 6 "normal" personality traits (Extraversion, Openness, Conscientiousness, Agreeableness, Neuroticism and Honesty-Humility), and the PID-5 [25 items, @hopwood2012] to measure "pathological" personality traits (Disinhibition, Antagonism, Detachment, Negative Affect and Psychoticism). The participants were the same as in study 2 (see **Figure 3**). However, due to a technical issue, no personality data was recorded for the first eight participants.

\begin{figure}
\includegraphics[width=1\linewidth]{figures/Figure3} \caption{The upper plots show the distribution of demographic and dispositional variables. The middle plots shows the illusion sensitivity scores as a function of sex and age (solid lines indicate significant relationships). Bottom plots show the correlation between the general factor of illusion sensitivity (Factor \textit{i}) and personality traits.}(\#fig:unnamed-chunk-4)
\end{figure}

## Data Analysis

For each of the individual illusion sensitivity scores (10 illusion-specific factors and the general Factor *i*), we tested the effect of contextual variables (screen size, screen refresh rate), demographic variables (sex, education, age) and personality. As the supplementary material contains the detailed results, we will only report the significant results [based on the Bayes Factor *BF* or the Probability of Direction *pd*, see @makowski2019indices].

## Results

The Bayesian correlation analysis (with narrow priors centered around a null effect) between the illusion scores and contextual variables (screen size and refresh rate) provided weak evidence in favor of an absence of effect, with the exception of the two contrast-based illusions. Anecdotal ($BF_{10} = 2.05$) and moderate evidence ($BF_{10} = 4.11$) was found for a negative correlation between screen size and the sensitivity to the White and the Contrast illusion, respectively. To test whether this result could be an artifact related to the highly skewed screen size distribution (caused by very few participants with extreme screen sizes), we re-ran a robust correlation (with rank-transformed values), which provided even stronger evidence in favor of the effect existence ($BF_{10} = 28.19$, $BF_{10} = 4.31$ for White and Contrast, respectively).

The Bayesian t-tests on the effect of sex suggested anecdotal to moderate evidence in favour of the null effect for all scores, with the exception of the sensitivity to the Zöllner illusion, which was higher in males as compared to females ($\Delta=-0.37$, 95% CI [-0.62, -0.13], $BF_{10} = 12.74$). We fitted Bayesian linear models with the education level entered as a monotonic predictor [appropriate for ordinal variables, @burkner2020modelling], which yielded no significant effects. For age, we fitted two types of models for each score, one general additive models (GAM) and a 2nd order polynomial model. These consistently suggested a significant positive linear relationship between age and Factor *i* ($pd=100\%$), as well as the sensitivity to Müller-Lyer ($pd=100\%$), Vertical-Horizontal ($pd=100\%$), Zöllner ($pd=100\%$) and Ebbinghaus ($pd=99\%$) illusions.

Regarding "normal" personality traits, Bayesian correlations suggested substantial evidence in favor of a positive relationship between *Honesty-Humility* and Zöllner ($BF_{10} > 100$), Vertical-Horizontal ($BF_{10} = 9.78$) and the Factor *i* ($BF_{10} = 4.00$); as well as between *Agreeableness* and Vertical-Horizontal ($BF_{10} = 25.06$), Ponzo ($BF_{10} = 4.88$) and the Factor *i* ($BF_{10} = 19.65$).

Regarding "pathological" personality traits, the results yielded strong evidence in favor of a negative relationship between illusion scores and multiple traits. *Antagonism* was associated with the sensitivity to Vertical-Horizontal ($BF_{10} > 100$), Müller-Lyer ($BF_{10} = 21.57$), Ponzo ($BF_{10} = 17.97$) illusions, and the Factor *i* ($BF_{10} = 55.45$); *Psychoticism* was associated with the sensitivity to Vertical-Horizontal ($BF_{10} = 66.63$) and Müller-Lyer ($BF_{10} = 35.59$) illusions, and the Factor *i* ($BF_{10} = 35.02$); *Disinhibition* was associated with the sensitivity to Vertical-Horizontal ($BF_{10} = 25.38$), Zöllner ($BF_{10} = 7.59$), Müller-Lyer ($BF_{10} = 5.89$) illusions, and the Factor *i* ($BF_{10} = 31.42$); and *Negative Affect* was associated with Zöllner ($BF_{10} = 62.04$), Vertical-Horizontal ($BF_{10} = 12.65$), Müller-Lyer ($BF_{10} = 3.17$), and the Factor *i* ($BF_{10} = 6.39$). The last remaining trait, *Detachment*, did not share any significant relationship with illusion sensitivity.

## Discussion

<!-- Context -->

We report significant links between inter-individual indices of illusion sensitivity and variables related to experimental context, demographic characteristics and personality. Firstly, screen size was found to have a significant negative relationship with the sensitivity to the two contrast-based illusions, namely the White and Contrast illusions. One possible explanation can be found in the mechanism by which visual systems filter through more low spatial frequencies when the size of the target object is small [@dixon2014]. As this filtering process excludes illumination information from visual processing, smaller screen sizes could yield artifactual changes in brightness perception, which in turn could attenuate the illusory effect of luminance-related illusions.

<!-- Demographic -->

Our results suggested an inconsistent pattern of non-significant sex-differences, with the exception of greater sensitivity of males as compared to females for the Zöllner illusion. Although we do not consider this result as significant given its specificity, we note that the existing literature reports, if any differences, that females exhibited greater illusion sensitivity [@lo2011; @miller2001; @papageorgiou2020]. This inconsistency could be due to past studies using a measure of illusion sensitivity that conflates the effect of illusions *per se* with the perceptual abilities involved in the task, for which gender-related differences can be found (in fact, the authors mention sex-differences in visuospatial strategies as the potential mechanism underlying their findings). On the contrary, the perceptual difficulty of the task and the illusion effect was independently modulated in our paradigm, and statistically dissociated. Our scores of illusion sensitivity might thus be less loaded with perceptual skills, thereby mitigating its effect.

<!-- Normal personality + Antagonism -->

Our findings also suggested a positive relationship between illusion sensitivity and two "normal" personality traits, namely *Honesty-Humility* and *Agreeableness*, and a negative link with *Antagonism*. Although the past literature regarding the links between illusion sensitivity and personality traits remain scarce, convergent evidence can be found in studies reporting a negative relationship between illusion sensitivity and hostility, aggression and narcissism [@zhang2017; @konrath2009seeing; @pessoa2008]. While this result's interpretation is challenging, one possible explanation could be drawn from the literature on the cognitive style known as field dependence. Since narcissism and aggression tendencies are correlated with lower field dependence [i.e., a lesser reliance on external cues in ambiguous contexts, @witkin1976; @ohmann2016; @damour2021], opposite traits, such as *Honesty-Humility* and *Agreeableness*, could conversely be more biased by contextual cues and thus more sensitive to illusions.

<!-- Pathological personality -->

The positive relationship between illusion sensitivity and "positive" personality traits is mirrored by a negative relationship with several other pathological traits, including *Psychoticism*, *Disinhibition*, and *Negative Affect*. These results are, in general, consistent with past findings and theories, suggesting a negative relationship between egocentric cognitive styles and context processing [including illusion sensitivity, @konrath2009seeing]. For instance, pathological egocentric beliefs [often observed alongside *Psychoticism*, @fox2006] have been related to reduced context integration [manifesting for instance in a tendency to separate objects from their surroundings when processing visual stimuli, @ohmann2016; @konrath2009seeing; @fox2006]. As such, it is possible to relate this higher resistance to illusions to a self-centered, decontextualized and disorganized information processing style, which can be found across the aforementioned maladaptive personality traits [@msetfi2009; @parkes1981field; @calamari2000field; @hoyle2006] .

Furthermore, these results in favour of a link between illusion sensitivity and maladaptive personality traits in a non-clinical population could be put in relation with clinical findings, which could be seen as extreme cases where the relationship with illusion sensitivity is the most manifest. In line with our results (in particular on *Psychoticism* and *Disinhibition*), prior research has found greater illusion resistance in schizophrenia [@notredame2014; @pessoa2008; @grzeczkowski2018], and in particular, in association with schizotypal traits, such as cognitive disorganization [@cretenoud2019; @lanyi2022can].

# General Discussion

<!-- Parametric framework -->

The parametric illusion generation framework developed in @makowski2021 proposes to conceptualize illusions as made of targets and distractors, both of which can be manipulated independently and continuously. In the present study, we have shown that such gradual modulation of illusion strength is effectively possible across 10 different types of classic visual illusions. This important methodological step opens the door for new illusions-based paradigms and tasks to study the effect of illusions under different conditions and to quantify illusion sensitivity using objective behavioral outcomes, such as accuracy or speed.

<!-- Factor i -->

Our findings suggest that the sensitivity to 10 different types of visual illusions share a common part of variance, supporting the existence of a general factor of illusion sensitivity (Factor *i*). This result comes in a field of mixed findings. In fact, contrary to early studies on visual illusions, more recent research have generally not found any significant evidence for a common stable factor across illusions within individuals [@grzeczkowski2017; @cretenoud2019; @cretenoud2020illusions; @grzeczkowski2018; @yang2012]. Instead, past findings suggest illusory effects are highly specific to the perceptual features of the illusions at stake [@grzeczkowski2017; @cretenoud2019]. It should be noted, however, that most of these studies were low-powered and/or relied on conventional paradigms, such as the adjustment procedure to measure the participants' subjective perception. We believe that our study presents several methodological improvements, including statistical power (high number of trials per participant), homogeneous stimuli (with minimal and highly controlled features) and tasks (decision-making reaction-time task), and a more reliable participant-level score extraction method (based on random-factors models), which in our opinion contributed to the emergence of the common factor.

However, although the illusions were relatively different in terms of the perceptual task (contrast-based, size-estimation, angle-perception), the possibility of our general factor being driven by inter-individual perceptual skills variability (or other cognitive skills) cannot be discarded. Future studies should investigate the relationship between perceptual abilities (in a similar task, but without illusions) and illusion sensitivity, and assess the psychometric properties of similar paradigms, including stability (e.g., test-retest reliability) and validity.

<!-- Personality -->

Finally, we found that the sensitivity to illusions was positively associated with "positive" personality traits, such as *Agreeableness* and *Honesty-Humility*, and negatively associated with maladaptive traits such as *Antagonism*, *Psychoticism*, *Disinhibition* and *Negative Affect*. Beyond highlighting the relevance of illusions beyond the field of visual perception, these results point towards an association with high-level general-domain mechanisms. While the search for the exact mechanism(s) underlying these links is an important goal of future research, our findings unlock the potential of illusion-based tasks as sensitive tools to capture specific inter-individual neuro-cognitive differences.

To conclude, we strongly invite researchers to explore and re-analyze our dataset with other approaches and methods to push the understanding of visual illusions and illusion sensitivity further. The task, data and analysis script are available in open-access at [**https://github.com/RealityBending/IllusionGameValidation**](https://github.com/RealityBending/IllusionGameValidation){.uri}.

# Acknowledgments

We would like to thank Tam Pham and Zen J. Lau for their contribution to *Pyllusion*, as well as Prof Dólos for the inspiration.

\newpage

# References

::: {#refs custom-style="Bibliography"}
:::