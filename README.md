# HRI Trust Empirical Studies Data

This repository contains the dataset used in the paper titled "Trust in Human-Robot Interaction: A Review and Analysis of Empirical Studies". The dataset is a CSV file containing information about 620 empirical studies on trust in human-robot interaction (HRI) conducted between 2015 and 2024.

## Dataset Overview

The dataset is a CSV file named `hri_trust_studies.csv`. Each row represents a unique empirical study focused on HRI trust. The columns contain detailed information about the study design, robot characteristics, task, level of interaction, trust assessment methods, and experimental manipulations. This level of detail allows for a variety of analyses and investigations into HRI trust.

### Data Columns

Here's a breakdown of the columns in the dataset:

**A. Study Information**

*   `Author`: The author(s) of the published study.
*   `Title`: The title of the published study.
*   `Publication Year`: The year the study was published.
*   `number_of_studies`: The number of distinct studies reported in the paper.

**B. Basic Study Information**

*   `initial_participants`: The total number of participants who were initially recruited or began the study.
*   `valid_participants`: The number of participants included in the final analysis after exclusions.
*   `excluded_participants`: The number of participants who were excluded from the final analysis.
*   `exclusion_reasons`: Reasons for participant exclusion (if any).
*   `data_collection_setting`: The setting where the data was collected. Options are: Online Crowdsourcing, Controlled Lab Environment, Real-World Environment, Educational Setting, Survey/Interview, or Other.
*   `experiment_design`: Study design (between-subjects, within-subjects, or mixed design).
*   `experimental_procedure`: A summary of the key experimental steps.
*   `experimental_task`: A description of the main task(s) participants completed.

**C. Robot Characteristics**

*   `robot_characteristics.robot_models`: The specific model(s) of robots used (e.g., Nao, Pepper, Baxter, Franka Emika Panda or 'Unspecified').
*   `robot_characteristics.robot_types`: The type(s) of robots used from the following categories: Humanoid Robots, Expressive Robots, Industrial Robot Arms, Mobile Robots, Mobile Manipulators, Autonomous Vehicles, Unmanned Aerial Vehicles (UAVs), Unmanned Ground Vehicles (UGVs), Collaborative Robots (Cobots), Service and Assistive Robots, Telepresence Robots, Legged Robots, Swarm Robots, Hybrid Robots, Soft Robots, and Other.
*   `robot_characteristics.robot_functions`: The main functions of the robot in the study, such as Educational, Industrial, Care, Research, Social, or Other.

**D. Experimental Setup Details**

*   **Interaction Intensity**
    *   `interaction_intensity.classification`: Level of interaction: "no interaction (text-only)", "passive observation", "minimal interaction", or "direct-contact interaction".
    *   `interaction_intensity.description`: A brief description of the interaction.

*   **Immersiveness**
    *   `immersiveness.classification`: Level of immersiveness: text-only, images, video, simulation, AR/VR, real-world.
    *   `immersiveness.description`: A brief description of the immersiveness.

*   **Robot Embodiment**
    *   `robot_embodiment.classification`: Type of robot embodiment: hypothetical, simulated, physical.
    *   `robot_embodiment.description`: Brief description of robot embodiment.

*   **Robot Autonomy Level**
    *   `robot_autonomy_level.classification`: Level of robot autonomy: not autonomous, pre-programmed (non-adaptive), wizard of oz (directly controlled), shared control (fixed rules), shared control (adaptive), fully autonomous (limited adaptation), or fully autonomous (adaptive).
    *   `robot_autonomy_level.description`: A brief description of the robot autonomy level.

**E. Task Classification**

*   `task_classification.high_level_task`: High-level task category: Social, Manipulation, Navigation, Teleoperation, Game, Supervision, Evaluation and Judgement, or Other.
*   `task_classification.sub_task`: Specific subtask for the corresponding high-level task category.

**F. Trust Assessment**

*   `trust_assessment.trust_measurement`: High-level method(s) used to measure trust: Questionnaires, Custom Scales, Behavioral Measures, Performance-Based Measures, Real-time Trust Measures, Physiological Measures, Multidimensional Measures, or Others.
*   `trust_assessment.trust_questionnaires_used`: Specific questionnaires used (if applicable). Standard questionnaire names are used here such as Trust Perception Scale - HRI, Trust in Automation Scale (TAS), etc.
*   `trust_assessment.data_collection_for_trust_modeling`: All data types collected for the purpose of trust modeling (Video Data, Physiological Signals, Eye-tracking Data, Speech Data, Performance Metrics, Robot Data, Other Data).
*   `trust_assessment.description`: Brief description of the overall approach to assessing trust in the study.

**G. Trust Modeling Approach**

*   `trust_modeling_approach.classification`: Approach used to model trust: no modeling, parametric models (e.g., regression), deep learning (e.g., neural networks, reinforcement learning), hidden markov model, or POMDP.
*   `trust_modeling_approach.description`: A brief description of the trust modeling approach.

**H. Research Type Classification**

*   `research_type.classification`: High-level research type: Empirical HRI Studies, Meta-Analysis & Review Studies, Observational & Survey Studies, or Other.
*   `research_type.subcategory`: Specific subcategory of the research type (e.g. Physical Robot Studies, Systematic Reviews etc.)

**I. Experimental Manipulation and Trust Influence**

*   `experimental_manipulation.manipulation_classification`: How the researchers influenced trust: Direct Manipulation, Indirect Manipulation, No Manipulation.
*   `experimental_manipulation.factors_manipulated`: Factors manipulated:   Robot-nonverbal-communication, Robot-emotional-display, Robot-social-attitude, Robot-social-timing, Robot-verbal-communication-content, Robot-verbal-communication-style, Robot-accuracy, Robot-task-strategy, Robot-interface-design, Robot-aesthetics, Robot-morality, Robot-autonomy, Robot-adaptability, Task-complexity, Task-constraints, Task-environment, Teaming or Other.
*   `experimental_manipulation.description`: Detailed description of what was manipulated or influenced in each study and how it was intended to affect trust.
*   `experimental_manipulation.impact_on_trust`: Reported effect of the experimental manipulations on trust (increased, decreased, or remained stable).
*   `experimental_manipulation.factors_that_impacted_trust`: Factors from 'factors_manipulated' that impacted trust.
*   `experimental_manipulation.factors_that_did_not_impact_trust`: Factors from 'factors_manipulated' that did not impact trust.
*  `experimental_manipulation.factors_description`: Detailed description of reasoning for choices of categories in factors_manipulated, factors_that_impacted_trust, and factors_that_did_not_impact_trust

**J. Additional Notes**

*   `additional_notes.notable_trends`: Any notable trends or unexpected results.
*   `additional_notes.key_findings`: The main result or conclusion of the study.
*   `additional_notes.task_description`: Description of what both the robot and the human did in the core task of the interaction.
*   `statistical_analysis.statistical_test`: The statistical tests applied in the study.
*   `statistical_analysis.test_description`: Brief description of statistical tests, including variables, and overall purpose of the tests.
*   `additional_notes.ecological_validity_assessment`: How the study design and setup influenced trust outcomes.

### Data Encoding Notes

*   **Text Fields:** Descriptions in the dataset are meant to be clear and concise but might contain subjective details, so consider cleaning it before analysis if needed.
*   **List Fields:** If multiple items are applicable they are presented as comma separated lists within a single cell.
*   **Categorical Fields:** Certain columns, such as `environment`, `interaction_intensity`, or `trust_measurement` have predefined, standardized categories. Make sure to consult this README when performing analysis.

## Example Queries

Here are some basic examples using Python with the Pandas library to help you get started:

**Filter studies by robot type:**

```python
import pandas as pd

df = pd.read_csv('hri_trust_studies.csv')
humanoid_studies = df[df['robot_characteristics.robot_types'].str.contains('Humanoid', na=False)]
print(humanoid_studies.head())
```

Analyze trust factors:

```python
import pandas as pd
df = pd.read_csv('hri_trust_studies.csv')
trust_factors = df['experimental_manipulation.factors_that_impacted_trust'].value_counts()
print(trust_factors)
```

We also provide a [Jupyter Notebook](hri_trust_data_exploration.ipynb) in this repository that demonstrates how to load and explore the dataset. Additionally, a separate [notebook] (hri_trust_paper_plots.ipynb) is available which generates the plots and latex tables used in the associated paper.

## License

This dataset is licensed under the MIT License. See the `LICENSE` file in the repository for details.

## Start Exploring!

We hope this dataset serves as a valuable resource for you! Start exploring the data, discover new insights, and contribute to the field of human-robot interaction.

Happy researching!