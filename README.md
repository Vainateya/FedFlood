# FedFlood
An early warning system for urban flood prediction using federated learning.

## Project Overview

(Note: This research was done within the Floodwatch research group at the University of Virginia) 

FedFlood is a research project focused on developing an advanced early warning system (EWS) for urban flood prediction using Federated Learning (FL). The project's primary objective is to enhance the accuracy of urban flood forecasting systems by utilizing federated learning with real-time data. This approach involves a novel hybridized deep learning method that features a hierarchical federated learning time-series model, which trains on real-time sensor data and weather station data. To this, it incorporates state-of-the-art non-ML methods like Copernicus (GloFAS), ensuring the inclusion of hydrological, meteorological, and satellite data to create a novel comprehensive early warning system for urban flood prediction. We test our system for real-time capabilities and accuracy in predicting historical flood events. For our experiment, we focused our efforts on the geographical area of Vietnam, ranked first in the world for exposure to riverine, flash, and coastal flooding. 

## Background:

Research has consistently demonstrated the efficacy and widespread use of machine learning (ML) in building early warning systems (EWS) for flood prediction. This is largely due to ML's ability to process vast amounts of data and identify patterns that traditional methods might miss. While much of the previous ML research on flood forecasting has focused primarily on riverine flooding, urban areas, with their high population densities, pose a particularly significant risk for flood-related disasters. This makes the development of EWS for urban areas critically important.

Empirical evidence supports this focus, as the absence of effective early warning systems in certain regions has been linked to mortality rates that are up to eight times higher compared to areas with such systems. However, creating a reliable EWS for urban flood prediction is inherently challenging. Such systems require extensive networks of reliable sensors to provide the real-time data necessary for accurate validation. This need for extensive sensor networks, however, involves considerable resources and infrastructure.

In situations where sensor data is limited or unavailable, models often rely heavily on established non-ML approaches, such as statistical, probabilistic, mathematical, or scientific models. While these models can be effective for issues like riverine or coastal flooding, they may not perform as well in urban environments due to the complexities and variability present. Therefore, a robust EWS for urban flood prediction semes to requires substantial real-time sensor data "local" to the urban environment to continuously validate and corroborate its predictions.

A simple solution might seem to be augmenting urban sensor data with data from other locations around the globe, creating a larger "global" foundation model that operates under the assumption that consistent features leading to flood prediction across these diverse data sources can still provide valuable insights for the model. However, this approach is not without its challenges.

The assumption that increasing the size of the dataset directly improves model performance does not hold true when dealing with data related to weather phenomena. The issue lies in data heterogeneity, which arises when training a large foundational model with data from various geographical locations. Data from one sensor may not be representative or relevant to data from another, leading to difficulties in creating a generalized model that performs well across different regions. This disparity in data distribution can significantly impact the model's accuracy and reliability, especially in diverse urban settings.

Federated learning offers a promising solution to the challenges of data heterogeneity and model generalization in urban flood prediction. By enabling the creation of multiple clients from sensors located worldwide, FL aggregates localized insights into a comprehensive global foundational model. This global model provides broad predictive capabilities, while local models retain specificity to their respective regions. In areas with limited access to sensor data, the global model, informed by trends from various local models, can still offer decent predictive capabilities. Conversely, in regions with abundant sensor data, local models can enhance their accuracy by fine-tuning based on the generalized insights provided by the global model. This symbiotic relationship inherent in federated learning setups helps balance the need for both generalization and specificity. The FedFlood project leverages this approach to enhance the accuracy and reliability of urban flood forecasting, ensuring that EWS systems are effective even in areas with varying levels of sensor data availability.

## Key Contributions:

1. Novel appraoch to balancing the issues of data heterogeneity and sensor dependency for urban flood prediction
2. FedFlood, A novel EWS for urban flood prediction, featuring the following:
 
   a) Demonstrated real-time predictive capacity validated by real-time data
   
   b) Time-series model within a Federated Learning framework
   
   c) Module-inspired hybrid deep learning approach
   
   d) Ensured data privacy and security

4. Study on optimal aggregation strategies for time-series flood prediction
5. Ablation study to clearly show the contribution of each component to the overall accuracy of FedFlood 

