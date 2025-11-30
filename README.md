# 💬 Gym Customer Feedback Insights: NLP Topic Modelling for Operational Improvement

---

## Project Background

This project applies **Natural Language Processing (NLP)** to analyse customer reviews for a large gym chain, aiming to identify recurring themes and operational pain points. By automating topic extraction from large volumes of textual data, the analysis supports actionable insights to improve customer experience, optimise facility operations, and guide strategic decisions.

The analysis consolidates location-level feedback, with a focus on **negative reviews** to identify critical areas for intervention.

---

## Objective

- Explore customer review datasets from multiple platforms  
- Perform frequency analysis and generate word clouds to visualise common terms  
- Apply BERTopic to model topics across reviews and identify recurring themes  
- Identify locations with the highest concentration of negative feedback  
- Validate findings with LDA topic modelling  
- Conduct emotion analysis to assess review sentiment and isolate anger-predicted reviews  
- Apply large language models (LLMs) to extract concise, actionable operational insights  

---

## Data Overview

- **Review Platforms:** Two sources of customer reviews  
- **Language Filter:** Only English-language reviews included  
- **Preprocessing:** Punctuation removal, number elimination, stopword filtering, tokenisation  

---

## Initial Data Investigation

- **Negative Review Frequency Analysis:**  
  - Isolated reviews with low ratings (<3)  
  - Frequent negative terms: Staff, Equipment, Machine, Membership, People

<img width="395" height="218" alt="image" src="https://github.com/user-attachments/assets/dd38b127-b951-47fe-ae11-69f8368f540b" />

<img width="395" height="218" alt="image" src="https://github.com/user-attachments/assets/ea6fd3e3-f727-4784-aafd-103b4a654d66" />

**Insight:** Negative feedback consistently highlights operational concerns related to staff, equipment, and facilities.

---

## Topic Modelling with BERTopic

- Merged reviews to ensure location-independent analysis  
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

**Insight:** Core operational issues consistently relate to staff, equipment, and facilities.

---

## Location-Level Analysis

- Identified top 20 locations with the highest negative review counts  
- Consolidated top 30 locations for analysis  
- BERTopic on top locations revealed:
  - **Dominant Topic (95.8%)**: Equipment, staff, and machine-related issues  
  - **Secondary Topic (4.2%)**: Parking and infrastructure complaints  

<img width="452" height="122" alt="image" src="https://github.com/user-attachments/assets/06b82103-ca9c-4fec-924d-0e37c0e122f4" />

**Insight:** Core dissatisfaction is consistent across high-complaint gyms; secondary issues are location-specific.

---

## Emotion Analysis

- Applied BERT-based emotion classifier to all reviews  
- Anger-predicted reviews modelled separately with BERTopic  
- Ten distinct anger-related topics identified:
  - Environmental failures: Cold showers, hygiene, noise complaints  
  - Immediate disruptions: Unexpected closures, unavailable equipment  
  - Physical discomfort: Temperature and cleanliness issues  

<img width="452" height="339" alt="image" src="https://github.com/user-attachments/assets/a89754c4-794f-41e9-baac-b32e54c965a5" />

**Insight:** Severe negative reactions are triggered primarily by immediate environmental failures, highlighting the need for real-time facility management.

---

## LLM Prompt-Engineered Insights (Phi-4-Mini-Instruct)

- Used an efficient LLM to process extracted topics and generate actionable insights  
- Applied prompt engineering to compress topic arrays into high-level recommendations [ADD IMAGE OF LLM INSIGHTS]  
- Workflow:
  - Extracted topic strings from reviews (`topic_string_array`)  
  - LLM grouped topics into actionable insights for operational priorities  

**Key LLM-Generated Insights:**

1. **Service Quality and Staff Behavior**  
   - Train staff to improve professionalism and responsiveness  
   - Implement conflict management and staff training programmes  

2. **Facility Maintenance and Cleanliness**  
   - Increase cleaning frequency and improve upkeep of locker rooms and showers  
   - Ensure proper ventilation and air conditioning  

3. **Equipment Quality and Maintenance**  
   - Maintain and repair equipment regularly  
   - Ensure variety and availability of equipment  

4. **Membership and Pricing**  
   - Review membership options for value  
   - Streamline cancellation and upgrade processes  

5. **Customer Experience and Communication**  
   - Improve response times from customer service  
   - Clarify membership terms and onboarding processes  

6. **Facility Management and Safety**  
   - Reduce overcrowding and improve space/equipment allocation  
   - Address security concerns and ensure staff response to incidents  

7. **Customer Satisfaction and Feedback**  
   - Collect and act on feedback systematically  
   - Address recurring dissatisfaction with service quality  

8. **Health and Safety Concerns**  
   - Maintain hygiene standards and monitor environmental safety  
   - Provide support for mental health and vulnerable members  

9. **Facility Cleanliness and Maintenance**  
   - Address maintenance issues such as mold and unclean facilities  

10. **Customer Service and Management**  
    - Strengthen staff training and overall management practices  

**Insight:** Prompt-engineered LLM modelling surfaces nuanced, actionable recommendations across service quality, facility management, equipment, and customer experience.

---

## Validation with LDA

- Applied Gensim LDA for probabilistic topic modelling  
- Generated 10 topics and interactive intertopic maps  
- Confirmed BERTopic findings with clear thematic separation  
- Most frequent terms: Equipment (~1400 mentions), Staff (~1200 mentions)  

<img width="903" height="571" alt="Screenshot 2025-11-30 at 12 06 43" src="https://github.com/user-attachments/assets/818422d9-e583-4100-b9da-26d6628ca5d8" />

**Insight:** Dual-method approach strengthens confidence in core pain points and confirms staff, equipment, and facilities as central operational concerns.

---

## Recommendations

- **Operational Focus:** Prioritise interventions on equipment availability, staff training, and facility maintenance ⚡  
- **Environmental Management:** Implement real-time monitoring to address immediate environmental failures (showers, temperature, cleanliness) ✅  
- **Membership & Access:** Simplify multi-gym access, day pass processes, and membership adjustments  
- **Safety & Hygiene:** Maintain high standards to mitigate health and safety risks  
- **Staff Conduct:** Address misconduct and behaviour through training and accountability  
- **Data-Driven Strategy:** Continuously monitor customer feedback using NLP pipelines 📈  
- **Resource Allocation:** Focus on high-complaint gyms while applying learnings across other locations  

---

## Key Takeaways

- Negative reviews consistently emphasise staff, equipment, and facilities  
- Emotion analysis highlights urgency of environmental and operational management  
- BERTopic, LDA, and LLM approaches improve clarity, reduce noise, and generate actionable insights  
- Recommendations provide a framework to prioritise interventions, optimise operations, and improve customer satisfaction
