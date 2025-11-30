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
- Use built-in BERTopic visualisations (intertopic maps, word scores, similarity heatmaps)
- Conduct LDA topic modelling for validation
- Perform emotion analysis to determine review sentiment and focus on anger-predicted reviews  
- Apply large language models (LLMs) to extract concise, actionable topics and recommendations

---

## Data Overview

- **Review Platforms:** Two sources of customer reviews  
- **Language Filter:** Only English-language reviews included  
- **Preprocessing:** Punctuation removal, number elimination, stopword filtering, tokenisation  

---

## Initial Data Investigation

- **Negative Review Frequency Analysis:**  
  - Isolated reviews with low ratings (<3) to identify critical feedback  
  - Frequent negative terms: Staff, Equipment, Machine, Membership, People

<img width="395" height="218" alt="image" src="https://github.com/user-attachments/assets/dd38b127-b951-47fe-ae11-69f8368f540b" />

<img width="395" height="218" alt="image" src="https://github.com/user-attachments/assets/ea6fd3e3-f727-4784-aafd-103b4a654d66" />

**Insight:** Negative feedback is consistent across platforms, highlighting recurring operational concerns.

---

## Topic Modelling with BERTopic

- Merged reviews across platforms to ensure location-independent analysis  
- Generated topic frequencies and visualisations
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

 <img width="452" height="122" alt="image" src="https://github.com/user-attachments/assets/06b82103-ca9c-4fec-924d-0e37c0e122f4" />

**Insight:** Core dissatisfaction is consistent across high-complaint locations, while secondary issues vary by location.

---

## Emotion Analysis

- Applied BERT-based emotion classifier to all reviews  
- Anger-predicted reviews extracted and modelled separately with BERTopic  
- Identified 10 distinct anger-related topics:
  - Environmental failures: Cold showers, hygiene, noise complaints  
  - Immediate disruptions: Unexpected closures, unavailable equipment  
  - Physical discomfort: Temperature and cleanliness issues  

<img width="452" height="339" alt="image" src="https://github.com/user-attachments/assets/a89754c4-794f-41e9-baac-b32e54c965a5" />


**Insight:** Most severe negative reactions are triggered by immediate environmental failures rather than systemic issues, emphasising the need for real-time facility management.

---

## Large Language Model Analysis (Prompt-Engineered Insights)

- Used a small, efficient LLM to process extracted topics and generate actionable business insights  
- Applied prompt engineering to compress and group topic arrays into high-level recommendations [ADD IMAGE OF LLM INSIGHTS]  
- Sample workflow:
  - Extracted topic strings from reviews (`topic_string_array`)  
  - Compressed topics via LLM with system prompt instructing: *“Group or compress the topics and return them as business insights for improvement”*  
  - Generated numbered list of actionable insights for operational priorities  

**Key LLM-Generated Insights:**

1. **Service Quality and Staff Behavior**  
   - Train staff to improve professionalism and customer service  
   - Address unprofessional behavior and ensure staff responsiveness  
   - Implement conflict management and staff training programmes  

2. **Facility Maintenance and Cleanliness**  
   - Increase cleaning frequency and improve facility maintenance  
   - Address hygiene issues, including locker and changing room upkeep  
   - Ensure proper ventilation and air conditioning  

3. **Equipment Quality and Maintenance**  
   - Maintain and repair equipment regularly to prevent malfunctions  
   - Ensure variety and availability of equipment  
   - Improve equipment quality and ensure correct use  

4. **Membership and Pricing**  
   - Review membership options and pricing for value  
   - Offer buddy programs and convenient payment methods  
   - Address membership cancellations and upgrade processes  

5. **Customer Experience and Communication**  
   - Enhance communication and response times from customer service  
   - Address billing and payment issues, including unexpected charges  
   - Improve onboarding and clarify membership terms  

6. **Facility Management and Safety**  
   - Reduce overcrowding and manage equipment/space availability  
   - Improve facility and equipment oversight, including locker rooms  
   - Address security concerns and staff response to incidents  

7. **Customer Satisfaction and Feedback**  
   - Actively collect and act on customer feedback  
   - Address recurring dissatisfaction with service quality  
   - Implement a structured feedback system  

8. **Health and Safety Concerns**  
   - Address hygiene and environmental safety issues  
   - Ensure supervision and safety measures, especially for vulnerable individuals  
   - Provide support for mental health and substance-related concerns  

9. **Facility Cleanliness and Maintenance**  
   - Improve cleanliness of showers, restrooms, and changing rooms  
   - Fix issues such as mold and general facility neglect  

10. **Customer Service and Management**  
    - Strengthen staff training and responsiveness  
    - Improve overall customer management and satisfaction  

**Insight:** Prompt-engineered LLM modelling surfaces nuanced, actionable recommendations, enabling prioritisation of operational improvements across service quality, facility management, equipment, and customer experience.

---

## Validation with LDA

- Applied Gensim LDA to tokenised reviews  
- Generated 10 topics and interactive intertopic maps
- Confirmed BERTopic findings with clear thematic separation  
- Top recurring terms: Equipment (~1400 mentions), Staff (~1200 mentions)
  
<img width="903" height="571" alt="Screenshot 2025-11-30 at 12 06 43" src="https://github.com/user-attachments/assets/818422d9-e583-4100-b9da-26d6628ca5d8" />


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
