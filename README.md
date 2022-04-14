# Topic_Modeling
LDA_Coherence, LDA_Perplexity

 * [Measurement of the number of topics in children"s speech using LDA and Affinity propagation algorithm](http://www.dbpia.co.kr/Journal/articleDetail?nodeId=NODE09301947) (LDA와 선호도 전파 알고리즘을 이용한 아동 발화의 화제수 측정)
 
   * `Se-Eun Oh`, `Tak-Sung Heo`, `Yoonkyoung Lee`, `Yu-Seop Kim`
   
-----------------------------------------------

## Data

 * Children's speech data collected by the Department of Speech Pathology at Hallym University (Topic - School life, family life, other/friends)
 
   * 1st, 3rd, and 5th grade group data (Korean)
   
     * Data example

        |    Turn    | Utterance  | Korean speech  | English speech |
        | :------: | :---: | :-----: | :------: |
        |  <학교>  |      | 검 학교생활은 어때?          | Examiner: How is your school life?
        |    1     |   1  | 아 재미없어요.              | Child: No fun.
        |          |      | 검 재미없구나. 그리고?       | Examiner: That's not fun. And?
        |    2     |   2  | 아 점심 먹고 양치하고        | Child: Eat lunch and brush my teeth
        |          |   3  | 아 근데 엄마 보고싶다.       | Child: And, I miss my mom.
        
-----------------------------------------------

## Latent Dirichlet Allocation

 * LDA Topic Modeling
 
   * In LDA, the number of topics K is defined by the user, but the purpose of the study is to measure the number of topics using coherence and perplexity to measure the number of topics in speech.
   
   * Set K to 3-29 (K starts at 3 because the minimum number of topics in the data used in this study is 3).
   
   * Equation (1), standardization, is performed on the values of coherence and perplexity with topics from 3 to 29 through LDA.
   
     * *Standardization(x) = (x - mean(x)) / std(x)* &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(1)
   
   * In Equation (2), the highest value is defined as the prediction result.
   
     * *f(co,pe) = Standardization(co) - Standardization(pe)* &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(2)

-----------------------------------------------

## Experiment Result

 * Comparison of the number of topics in speech according to school age
 
    |   Grade (age)  | LDA | Speech pathology  |
    | :-----: | :--: | :-----: |
    |    1 (8)    |  19  | 19.5 |
    |    3 (10)   |   4  | 17.2 |
    |    5 (12)   |   4  | 12.5 |
    
    **The correlation coefficient between LDA and speech pathology - 0.7525**
    
-----------------------------------------------

## Conclusion

  * When looking at the correlation coefficient between LDA topic modeling and speech pathology, a high correlation coefficient was confirmed.
  
  * However, since the number of topics in the 3rd and 5th graders in LDA is the same, it is necessary to explore different topic modeling.
  
  * In future study, we plan to experiment with more sophisticated topic modeling, and through this, we will explore how to automate the number of topics.
   
