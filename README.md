# 💬 Customer Feedback Insights: NLP Topic Modelling for Operational Improvement

---

## Project Background

This project applies **Natural Language Processing (NLP)** techniques to analyse customer reviews, aiming to identify recurring themes and operational pain points. By automating topic extraction from large volumes of textual data, the analysis supports actionable insights for improving customer experience, optimising operations, and guiding strategic decisions.

The analysis covers reviews from multiple platforms, consolidates location-level feedback, and focuses on **negative reviews** to pinpoint the most critical issues.

---

## Objective

- Explore customer review datasets from multiple platforms  
- Perform frequency analysis and generate word clouds to visualise common terms  
- Apply BERTopic to model topics across reviews and identify recurring themes  
- Identify locations with the highest concentration of negative feedback  
- Use built-in BERTopic visualisations (intertopic maps, word scores, similarity heatmaps) [ADD IMAGE OF INTERTOPIC MAP]  
- Conduct LDA topic modelling for validation [ADD IMAGE OF LDA INTERTOPIC MAP]  
- Perform emotion analysis to determine review sentiment and focus on anger-predicted reviews  
- Apply large language models (LLMs) to extract concise, actionable topics and recommendations [ADD IMAGE OF LLM SUMMARY]  

---

## Data Overview

- **Review Platforms:** Two sources of customer reviews  
- **Language Filter:** Only English-language reviews included  
- **Preprocessing:** Punctuation removal, number elimination, stopword filtering, tokenisation  

---

## Initial Data Investigation

- **Frequency Analysis:**  
  - Common themes across platforms: Equipment, Staff, Facilities, Membership, Classes  
  [ADD IMAGE OF WORD CLOUD]  

- **Negative Review Focus:**  
  - Isolated reviews with low ratings (<3) to identify critical feedback  
  - Frequent negative terms: Staff, Equipment, Facilities, Membership, Access issues  
  [ADD IMAGE OF NEGATIVE WORD CLOUD]  

**Insight:** Negative feedback is consistent across platforms, highlighting recurring operational concerns.

---

## Topic Modelling with BERTopic

- Merged reviews across platforms to ensure location-independent analysis  
- Generated topic frequencies and visualisations [ADD IMAGE OF TOPIC FREQUENCY MAP]  
- Ten topics emerged:
  1. Cleanliness & Facilities – Hygiene complaints in showers, toilets, changing rooms  
  2. Buddy/Referral System – Referral programmes and friend account setup  
  3. Day Pass & Access – Short-term passes and visitor entry  
  4. Staff & Trainers – Service experiences and staff interactions  
  5. Classes & Scheduling – Group fitness booking and instructor quality  
  6. Membership Plans – Access levels and multi-gym usage rights  
  7. Cancellations – Membership termination difficulties  
  8. Equipment & Crowding – Machine availability and overcrowding  
  9. Broken Machines – Equipment maintenance issues  
  10. Air Conditioning & Temperature – Environmental comfort complaints  

**Insight:** Core operational issues focus on staff, equipment, and facilities.

---

## Location-Level Analysis

- Identified top 20 locations with highest negative review counts  
- Merged location data to create consolidated top 30 list  
- BERTopic modelling on top 30 locations revealed:
  - **Dominant Topic (95.8%)**: Equipment, staff, and machine-related issues  
  - **Secondary Topic (4.2%)**: Parking and infrastructure complaints  
  [ADD IMAGE OF TOP LOCATION TOPICS]  

**Insight:** Core dissatisfaction is consistent across high-complaint locations, while secondary issues vary by location.

---

## Emotion Analysis

- Applied BERT-based emotion classifier to all reviews  
- Anger-predicted reviews extracted and modelled separately with BERTopic  
- Identified 10 distinct anger-related topics:
  - Environmental failures: Cold showers, hygiene, noise complaints  
  - Immediate disruptions: Unexpected closures, unavailable equipment  
  - Physical discomfort: Temperature and cleanliness issues  
  [ADD IMAGE OF ANGER TOPIC CLUSTERS]  

**Insight:** Most severe negative reactions are triggered by immediate environmental failures rather than systemic issues, emphasising the need for real-time facility management.

---

## Large Language Model Analysis

- Used a small, efficient LLM to process reviews and extract concise topics  
- Sampled reviews to create a comprehensive topic array  
- BERTopic on LLM outputs reduced noise and clarified operational pain points  
- Extracted actionable categories:
  1. Equipment Scarcity – Availability constraints  
  2. Staff Misconduct – Behavioural problems and security concerns  
  3. Value Proposition – Pricing and membership complaints  
  4. Facility Amenities – Showers, towels, accessibility  
  5. Environmental Quality – Cleanliness and atmosphere concerns  
  6. Health & Safety – Welfare and hygiene risks  
  7. Facility Adequacy – Capacity and demographic-specific issues  
  8. Maintenance Standards – Cleaning frequency and upkeep failures  
  [ADD IMAGE OF LLM TOPIC EXTRACTION]  

**Insight:** LLM-assisted modelling surfaces serious hidden issues such as staff misconduct and safety risks, enabling prioritised operational responses.

---

## Validation with LDA

- Applied Gensim LDA to tokenised reviews  
- Generated 10 topics and interactive intertopic maps [ADD IMAGE OF LDA VALIDATION MAP]  
- Confirmed BERTopic findings with clear thematic separation  
- Top recurring terms: Equipment (~1400 mentions), Staff (~1200 mentions)  

**Insight:** Dual-method approach strengthens confidence in core pain points and validates that equipment, staff, and facilities are central operational concerns.

---

## Recommendations

- **Operational Focus:** Prioritise interventions on equipment availability, staff training, and facility maintenance ⚡  
- **Environmental Management:** Implement real-time monitoring to address immediate environmental failures (showers, temperature, cleanliness) ✅  
- **Customer Access & Membership:** Simplify multi-gym access, day pass processes, and membership adjustments  
- **Safety & Hygiene:** Maintain high standards to mitigate health and safety risks  
- **Staff Conduct:** Address misconduct and behavioural issues through training and accountability  
- **Data-Driven Strategy:** Continuously monitor customer feedback using NLP pipelines to identify emerging issues 📈  
- **Resource Allocation:** Focus on high-complaint locations while applying learnings across similar gyms  

---

**Key Takeaways**

- Negative reviews consistently emphasise staff, equipment, and facilities  
- Emotion analysis highlights urgency of environmental and operational management  
- Combining BERTopic, LDA, and LLM approaches improves clarity, reduces noise, and enhances actionable insights  
- Recommendations provide a framework to prioritise interventions, optimise operations, and improve customer satisfaction
