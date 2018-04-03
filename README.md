# dojo-naive-bayes-redis

## domain


### naive bayes

    p(category given observation) = 
        p(category) * p(observation given category) / p(observation)  
    
    p(observation given category) = 
        let p = 1 for feature in observation : p *= p(feature given category)
    
    p(observation) = 
        let p = 1 feature in observation: p *= p(feature)
    
    
    p(feature) = 
        nb(observation with feature) / nb (all observation)
    
    p(category) = 
        nb(observation labeled category) / nb (all observation)
    
    p(featue given category) = 
        nb(observation with feature, labeled category) / nb (observation labeled category)
    
    
### a negation of feature  (!feature)
    p(!feature) = 1 - p(feature)
    if (feature in not observation) => feature in not observation   
    
## backlog 

 1) reporting a labeled observation to a naive bayes model instance
 2) invoking a model instance to get the probabilities of each category given an input unlabeled observation 
 3) capability to scale (supporting load)  
 4) getting a metadata for model instance
 5) reporting a unlabeled observation to a naive bayes model instance then set label later

## Constraint 

  - TDD ( unit test ) no integration test needed
  - Pear programing or mob programing 
  - using REST api 
  - storing date in memory for US 1 and 2, and a key value db (redis like) for US 3,4,and 5