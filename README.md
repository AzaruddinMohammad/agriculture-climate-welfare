# Agriculture-Climate-Welfare (India)

this prototype is a **data-driven question answering system** that connects climate data (IMD) + agriculture production data (Ministry of Agriculture & Farmers Welfare) and answers policy-grade questions like:

- compare rainfall in 2 states over N years
- identify which district has highest/lowest production of Crop_Z
- analyze crop trends vs rainfall/climate shift
- generate arguments for switching from crop_A → crop_B using historical evidence

### Phase 1: Data Discovery & Integration
this system connects to datasets from:
- data.gov.in → Agriculture production
- data.gov.in → IMD rainfall datasets

**challenge:** both datasets are not aligned (codes, spelling, formats differ) so the system uses mapping + normalization logic to let them talk to each other.

### Phase 2: Intelligent Q&A System
user enters a natural language question → system:
1. classifies question type  
2. identifies which dataset is needed  
3. pulls relevant slices  
4. aggregates & answers with citations  

### Why this matters
India policy decisions require data evidence  
(not gut feeling)

our system generates **traceable answers** that include source dataset references.

### how to run (local development)
```bash
python -m venv venv
source venv/bin/activate        # windows: venv\Scripts\activate
pip install -r requirements.txt
streamlit run app.py
