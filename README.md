# shell-ai-hackathon-2024

Hello!

This is our submission to the **Shell.ai Hackathon for Sustainable and Affordable Energy 2024.**

The 5th edition of the Shell.ai Hackathon set an ambitious goal – using digital solutions and AI, they challenge participants to help build a lower-carbon world where everyone can access and afford energy.

**Problem statement**

Road transport is the backbone of supply chain, playing a pivotal role in moving goods and bolstering the economy. In this hackathon, we had a chance to develop mathematical models to optimize fleet decarbonization strategies and help fleet owners make informed decisions that align with their energy transition objectives and business outcomes.

(The full problem statement shared by Shell.ai for this hackathon has been uploaded to <a href="https://github.com/oregontoni/shell-ai-hackathon-2024/blob/main/Fleet%20Transition%20Challenge%20-%20problem%20statement.docx">this repository</a> and is also available on the hackathon's <a href="https://www.hackerearth.com/challenges/competitive/shellai-hackathon-2024/machine-learning/fleet-transition-challenge-9-975cec9c/">official webpage</a>.)

**Challenge**

Professional, delivery, and operational fleets are a significant contributor to global greenhouse emissions. Fleet owners aspire to achieve net-zero emissions promptly; however, the transition presents a complex dilemma. Balancing the urgency of achieving net-zero emissions with business
sustainability and customer satisfaction requires a decision-making framework that considers factors such as timing, location, and approach.

We received annual data from a fleet operator detailing operational demands that must be met for years 2023 to 2038. We also had to ensure that yearly CO2 emission thresholds were not exceeded by balancing the 3 drivetrains and their different emission levels in the fleet: Diesel, LNG, and BEV (Battery Electric Vehicle). Other additional constraints also had to be respected within the optimization model.

**Constraints**

1. Vehicle of size Sx can only cater to the demand of size bucket Sx.
2. Vehicles belonging to distance bucket Dx can satisfy all demands for distance bucket D1 to Dx. For example, a vehicle belonging to distance bucket D4 can satisfy the demand of D1, D2, D3, D4 buckets; similarly, D3 can satisfy D1, D2, D3 but NOT D4.
3. Total yearly demand for each year must be satisfied for each of the distance and size buckets.
4. A vehicle model of year 20xx can only be bought in the year 20xx. For example, Diesel_S1_2026 can only be bought in 2026.
5. Every vehicle has a 10-year life span and must be sold by the end of 10th year.
6. All Buy operations happen at the beginning of the year and all Sell operations happen at the end of the year.
7. Each year, at most 20% of the vehicles in the existing fleet can be sold.

**Timeline**
The hackathon launch webinar was on 31 May, 2024. Final submissions were due by 1pm on 01 Jul, 2024.

**Participants**
According to <a href="https://www.hackerearth.com/challenges/competitive/shellai-hackathon-2024/leaderboard/page/1/">HackerEarth</a>, more than 1,000 teams from around the world registered for the Shell.ai 2024 Decarbonisation hackathon.

*Team Mission Zero members*:

- Laura Ansari
- Toni Chan
- Charlie Liao
- Victor Morales


**Team Collaboration**

Tech Stack:
- Google Suite (Gdrive, Colab, Meet, TasksBoard)
- VS code
- Jupyter notebook

Coding of the solution:
- objective function (Charlie)
- constraints 1-4 (Laura)
- constraints 5-8 (Toni)

**Getting started**

To run our code, please run the following commands:

```shell
conda-lock install -n shell-ai-hackathon-2024
conda install -n shell-ai-hackathon-2024 conda-forge::pulp
```

**Our solution**

In this repository, you can find the following files:

- Datasets (provided by Shell):

    - carbon_emission.csv
    - cost_profile.csv
    - demand.csv
    - fuels.csv
    - vehicles_fuels.csv
    - vehicles.csv

- shell_hackathon_last_30points.ipynb: Python notebook that includes the optimization model
- shell_hackathon_output_30.csv: the output file that we uploaded as our final submission to the hackathon website