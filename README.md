<img width="604" alt="image" src="https://github.com/user-attachments/assets/bf6e27c7-6c63-40a6-b677-2069bb205292" /><img width="147" alt="image" src="https://github.com/user-attachments/assets/f97607d7-e8f1-4a40-969c-aff5ac0a7e7b" /># Data-Analyst-INDIEZ
### Case Study 1:
  1. All users in Russia and using Android devices are playing the game with version 1.5.2.
  2. Imagine you are a LiveOps team member and after working on data of game version 1.5.2, you found that the tutorial
  was not good for the users experience.
  3. Hence, you decided you would roll out a new version 1.6.0 to change the Tutorial in-game and you expected this
  would help increase user experience.

**Special Information: <br/>**
The game version 1.6.0 has rolled out 50% since 28-10-2023, meaning 50% of new users will keep playing game
version 1.5.2 and 50% of the remaining will play the new version 1.6.0.
You started collecting the data from 28-10-2023 to 10-11-2023 to analyze

**QUESTIONS**
1. How can we know if the improvement of Tutorial in-game version 1.6.0 has impacted the User Experience better
than in-game version 1.5.2? 
2. Can we roll out 100% game version 1.6.0 to all users or not? Why?
3. Based on the data and your experience with the game, do you have any ideas to improve our User Experience?

**DATA SOURCE <br/>**
This is private data so i can't share right now.

**TOOLS <br/>**
Python (pandas, numpy,...)

**PROBLEM SOLVING <br/>**
The goal of this analysis is to determine if the changes in version 1.6.0, particularly in the tutorial, have impacted the User Experience compared to the 1.5.2 version.

1. How can we know if the improvement of Tutorial in-game version 1.6.0 has impacted the User Experience (UE) better
than in-game version 1.5.2? <br/>
 The improvement of the Tutorial has impacted the UE through these key performance indicator, Daily Active User (DAU), Tutorial Complete Rate (TCR) and Retation Rate (compare day 1 to day 7) <br/>
 **a) The Tutorial Complete Rate (TCR):**
   
 ![image](https://github.com/user-attachments/assets/2dbea0f2-daa4-4836-b715-cc8592465e76)
 <img width="221" alt="image" src="https://github.com/user-attachments/assets/55e7585f-1445-4609-a8f2-6e4d4670395b" /> <img width="221" alt="image" src="https://github.com/user-attachments/assets/79c965a7-8423-487f-b18c-a037d050c75b" /> <br/>
The TCR of the 1.6.0 version is slightly higher than the previous one, which indicates that the improvement of the tutorial has positively impacted the UE. You can easily see that users have completed all the steps in the tutorial (8 steps compared to 4) in the new version. The potential reasons for this improvement include better clarity and interactivity of the tutorial steps, which make players feel engaged and motivated to continue playing.

**b) The Retention Rate (RR):** <br/>
<img width="239" alt="image" src="https://github.com/user-attachments/assets/5ff4d55e-2b9e-4abb-8e74-2cabe8ad310a" /> <img width="189" alt="image" src="https://github.com/user-attachments/assets/8aff50c8-bc07-4625-a1e6-354b76008ce0" />
 <br/>
The Retention Rate (RR) in the new version is higher than in version 1.5.2 (0.28 compared to 0.26 on day 1; 0.04 compared to 0.02 on day 7). This means users are more willing to play and stay in the game. Additionally, I applied the two-sample z-test to further conclude that the Retention Rate has a statistically significant impact on both day 1 and day 7. <br/>

**c) The Daily Active User (DAU):** <br/>
![image](https://github.com/user-attachments/assets/4f13256d-3a1e-400d-b96d-73465272a2a0)
 <br/>
Visualy we can see the number of active user of the 1.6.0 is higher than 1.5.2 <br/>

With all the information above, we can conclude that the improvement of the tutorial in version 1.6.0 has positively impacted the User Experience more than version 1.5.2.
2. Can we roll out 100% game version 1.6.0 to all users or not? Why? <br/>
Base on the analysis: <br/>
The 1.6.0 version has a significant improvement in Day 1 and Day 7 retention rates, indicating better user engagement. <br/>
The TCR shows that the new tutorial is effective. <br/> <br/>
**Recommendation:** <br/>
- Before releasing a new version, it's necessary to let veteran players, testers, and those who understand all the metrics of this game experience the beta version first. Then, adjust all the metrics before finally rolling it out. 
- When rolling out a new version, besides improving the game tutorial to attract new players, it's important to add features and missions to create challenges for existing players in order to enhance the user experience.


### Case Study 3:
Problem: Creative Optimization and Statistical Significance Testing
You are a Data Analyst at a mobile game development company. The company is running a Facebook Ads campaign to
promote a new game. You are tasked with conducting an A/B test to optimize creatives (ad images and videos). <br/>

Creative A: An image ad featuring a game character with the slogan "Join the adventure now!" <br/>
Creative B: A 15-second video ad showcasing gameplay and key game features. <br/> <br/>

Test Results: <br/>

Creative A <br/>
- Impressions: 50,000
- Clicks: 2,000
- Installs: 500
- Cost: $2,000 <br/>
<br/>


Creative B <br/>
- Impressions: 50,000
- Clicks: 3,000
- Installs: 600
- Cost: $2,000 <br/>

1. Calculate the following metrics for each creative:
- Click-Through Rate (CTR)
- Conversion Rate (CR)
- Cost Per Install (CPI)
2. Use the Statistics test to check whether the difference in Conversion Rate between the two creatives is statistically
significant. <br/>
Based on the statistical tests, which creative would you recommend for the next campaign?

**PROBLEM SOLVING <br/>**


**Metrics Definition:** <br/>
    Click_through_rate(ctr) = (click/impression)*100 <br/>
    Conversion_rate(cr) = (install/click)*100 <br/>
    Cost_per_install = (cost/install)*100 <br/> <br/> 

**Metrics Calculation:** <br/>

<img width="147" alt="image" src="https://github.com/user-attachments/assets/838633ce-e41e-4608-b2e3-abcaca9ceb47" /> <br/>

**Statistics Check:** <br/> 

<img width="604" alt="image" src="https://github.com/user-attachments/assets/5cc8fe25-e15c-4f12-919c-73c634ece817" /> <br/>


In this case, our goal is to compare the conversion rates of two creatives, which means we are comparing two proportions (installs/clicks). The z-test for proportions is specifically designed to test whether the difference between two proportions is statistically significant, so we are going to use it to reach our goal. <br/>

- Null Hypothesis: There is no difference in the Conversion Rates between Creative A and B <br/>
- Alternative Hypothesis: There a diffrence in the Conversion Rates between Creative A and B <br/>

**Conclusion:** <br/>
- p-value < 0.05: Reject Null Hypothesis. The difference in Conversion Rate between 2 Creative is statistically significant. <br/>

**Recomendation:** <br/>

Creative B has a higher CTR (6% vs. 4%) and a lower CPI ($3.33 vs. $4 per install), indicating it attracts more clicks and is more cost-effective than Creative A. <br/>

Creative A has a higher CR (25% vs. 20%), suggesting that users who click on Creative A are more likely to install the game compared to Creative B. <br/>
 
So, for the next campaign, if the goal is to maximize clicks and installs with effective cost, I will use Creative B. If the goal is to optimize the Conversion Rate, I will use Creative A. <br/>








