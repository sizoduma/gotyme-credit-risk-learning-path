# 🏦 GoTyme Senior Data Scientist Learning Path
## Credit Risk Modeling & IFRS 9 ECL Framework

**Position:** Senior Data Scientist - Credit Risk Analytics  
**Company:** GoTyme MCA (South Africa)  
**Last Updated:** August 2026  
**Duration:** 16 Weeks Structured Learning  

---

## 📋 Executive Overview

This curated learning path combines the **most relevant, production-ready GitHub repositories** with a structured 16-week curriculum. It's designed to equip you with:

- ✅ **Credit Risk Modeling** (PD, LGD, EAD estimation)
- ✅ **IFRS 9 ECL Compliance** (Staging logic, regulatory calculations)
- ✅ **Model Interpretability & Governance** (SHAP, auditing, documentation)
- ✅ **MLOps & Monitoring** (Drift detection, model performance tracking)
- ✅ **Production Deployment** (End-to-end pipelines, automation)
- ✅ **Merchant Cash Advance** (MCA-specific patterns and risk drivers)

---

## 🗺️ Learning Path Overview

### **PHASE 1: FOUNDATIONS (Weeks 1-2)**
- Week 1: Python ML Fundamentals & Credit Risk Basics
- Week 2: Feature Engineering & Data Pipelines for Credit Risk

### **PHASE 2: CREDIT RISK FOUNDATIONS (Weeks 3-5)**
- Week 3: Credit Risk Scoring Models
- Week 4: Loss Given Default (LGD) & Exposure at Default (EAD) Modeling
- Week 5: IFRS 9 ECL Fundamentals & Staging Logic

### **PHASE 3: MODEL GOVERNANCE & INTERPRETABILITY (Weeks 6-8)**
- Week 6: Model Explainability & Interpretability
- Week 7: Model Governance & Documentation Standards
- Week 8: Stress Testing & Scenario Analysis

### **PHASE 4: PRODUCTION MLOPS & MONITORING (Weeks 9-12)**
- Week 9: MLOps Architecture & Data Pipelines
- Week 10: Model Monitoring & Drift Detection
- Week 11: Model Retraining & Deployment Pipeline
- Week 12: End-to-End Portfolio Analytics & Dashboards

### **PHASE 5: GOTYME-SPECIFIC APPLICATIONS (Weeks 13-15)**
- Week 13: Merchant Cash Advance (MCA) Credit Risk Modeling
- Week 14: Policy Experiments & A/B Testing
- Week 15: Governance & Regulatory Alignment (BSP/IFRS 9)

### **PHASE 6: CAPSTONE PROJECT (Week 16)**
- Week 16: End-to-End Credit Risk System Implementation

---

## 📚 Key Repositories (Ranked by Priority)

### **Tier 1: MUST STUDY (Critical for role)**

1. **TsoareloAdriaan11/IFRS9-ECL-ENGINE** ⭐⭐⭐⭐⭐
   - **URL:** https://github.com/TsoareloAdriaan11/IFRS9-ECL-ENGINE
   - **Why:** South African context, production-grade IFRS 9 implementation
   - **Key Features:** XGBoost PD modeling, SHAP explainability, Streamlit dashboard, CI/CD
   - **Time Allocation:** 15 hours across Weeks 5, 9-12, 16

2. **Daniel11OSSE/ifrs9-ecl-modeling** ⭐⭐⭐⭐⭐
   - **URL:** https://github.com/Daniel11OSSE/ifrs9-ecl-modeling
   - **Why:** Complete ECL framework with PD/LGD/EAD/Staging/Scenarios
   - **Key Features:** 4-scenario analysis, lifetime ECL calculation, stress testing
   - **Time Allocation:** 10 hours across Weeks 4-5, 8

3. **MAIF/shapash** ⭐⭐⭐⭐⭐
   - **URL:** https://github.com/MAIF/shapash
   - **Why:** Production-grade model explainability & governance
   - **Key Features:** SHAP/LIME integration, HTML audit reports, SmartPredictor deployment
   - **Time Allocation:** 12 hours across Weeks 6, 16

4. **jomariya23156/full-stack-on-prem-cv-mlops** ⭐⭐⭐⭐⭐
   - **URL:** https://github.com/jomariya23156/full-stack-on-prem-cv-mlops
   - **Why:** Complete MLOps ecosystem (data → model → monitoring)
   - **Key Features:** DVC, MLflow, Prefect, FastAPI, Evidently, Grafana, Docker
   - **Time Allocation:** 15 hours across Weeks 9-12, 16

### **Tier 2: STRONGLY RECOMMENDED (Deep expertise)**

5. **scikit-learn/scikit-learn** ⭐⭐⭐⭐⭐
   - **URL:** https://github.com/scikit-learn/scikit-learn
   - **Time Allocation:** 10 hours (Week 1, reference throughout)

6. **rasbt/python-machine-learning-book-3rd-edition** ⭐⭐⭐⭐⭐
   - **URL:** https://github.com/rasbt/python-machine-learning-book-3rd-edition
   - **Time Allocation:** 8 hours (Weeks 1-2)

7. **ageron/handson-ml3** ⭐⭐⭐⭐⭐
   - **URL:** https://github.com/ageron/handson-ml3
   - **Time Allocation:** 6 hours (Weeks 1-2)

### **Tier 3: SPECIALIZED TOPICS (Targeted deep dives)**

8. **fedeghigo/Credit-Risk.Machine-learning-application** ⭐⭐⭐⭐
9. **fischlerben/Machine-Learning-Credit-Risk** ⭐⭐⭐⭐
10. **krishnaveni-sk/credit-risk-shap-lime** ⭐⭐⭐⭐
11. **SharvenRane/model-monitoring** ⭐⭐⭐⭐
12. **Kiruba-Manimaran/financial-risk-stress-testing-model** ⭐⭐⭐⭐

---

## 🎯 Weekly Study Schedule

### **Time Commitment: 50 hours/week**

```
Monday-Friday (10 hours/day):
  09:00-10:00  Theory reading (repo docs, papers)
  10:00-12:00  Code study & annotation
  12:00-13:00  Lunch break
  13:00-15:30  Hands-on implementation
  15:30-16:00  Break
  16:00-17:30  Exercises & mini-projects
  17:30-18:00  Documentation & reflection

Saturday-Sunday (5 hours/day):
  Morning: Review & consolidation
  Afternoon: Advanced topics / optional deep dives
```

---

## 📊 Learning Outcomes by Phase

### **Phase 1: Foundations (Weeks 1-2)**
**Learning Outcomes:**
- [ ] Understand ML classification fundamentals (Logistic Regression, Trees, Ensemble)
- [ ] Master scikit-learn API for model building
- [ ] Implement robust feature engineering pipelines
- [ ] Handle class imbalance (SMOTE, class weights)
- [ ] Evaluate models using credit-specific metrics (Gini, KS, AUC)

**Deliverable:** Basic credit scoring model (Gini > 0.60)

---

### **Phase 2: Credit Risk Foundations (Weeks 3-5)**
**Learning Outcomes:**
- [ ] Build PD models using multiple algorithms
- [ ] Implement LGD regression models
- [ ] Model EAD using CCF approach
- [ ] Understand IFRS 9 three-stage classification
- [ ] Apply SICR triggers and staging logic
- [ ] Calculate 12-month vs. Lifetime ECL
- [ ] Implement scenario weighting for ECL

**Deliverable:** Complete IFRS 9 ECL calculator with PD/LGD/EAD models

---

### **Phase 3: Model Governance & Interpretability (Weeks 6-8)**
**Learning Outcomes:**
- [ ] Create SHAP explanations for credit decisions
- [ ] Generate model audit reports
- [ ] Document model development & governance
- [ ] Implement stress testing frameworks
- [ ] Design 4-scenario economic overlays
- [ ] Create sensitivity analysis reports

**Deliverable:** Governance-ready model documentation (30+ pages)

---

### **Phase 4: Production MLOps & Monitoring (Weeks 9-12)**
**Learning Outcomes:**
- [ ] Design production ML architecture
- [ ] Implement data versioning (DVC)
- [ ] Set up experiment tracking (MLflow)
- [ ] Orchestrate workflows (Prefect)
- [ ] Implement drift detection (PSI, KL divergence)
- [ ] Deploy models via FastAPI
- [ ] Monitor performance in production
- [ ] Build real-time dashboards

**Deliverable:** End-to-end production system with monitoring

---

### **Phase 5: GoTyme-Specific Applications (Weeks 13-15)**
**Learning Outcomes:**
- [ ] Engineer MCA-specific credit features
- [ ] Build segment-specific credit models
- [ ] Design approval & pricing scorecards
- [ ] Implement policy experiment framework
- [ ] Align models with BSP/IFRS 9 requirements
- [ ] Create regulatory compliance documentation

**Deliverable:** MCA credit risk system + regulatory compliance package

---

### **Phase 6: Capstone Project (Week 16)**
**Learning Outcomes:**
- [ ] Integrate all components into unified system
- [ ] Deploy production-ready credit decision API
- [ ] Create executive dashboards
- [ ] Implement governance workflows
- [ ] Document entire system (100+ pages)

**Deliverable:** Complete, production-ready credit risk system

---

## 🔧 Technical Stack

**Core Libraries:**
- scikit-learn (ML models)
- XGBoost, LightGBM (Gradient boosting)
- pandas, NumPy (Data processing)
- SHAP, LIME (Model explainability)

**MLOps Stack:**
- DVC (Data versioning)
- MLflow (Experiment tracking)
- Prefect (Workflow orchestration)
- FastAPI (API development)
- Streamlit (Web dashboards)

**Monitoring & Governance:**
- Evidently AI (Drift detection)
- Prometheus, Grafana (System monitoring)
- pytest (Testing)
- GitHub Actions (CI/CD)

**Databases:**
- SQLite (Local development)
- PostgreSQL (Production)
- Parquet (Feature storage)

---

## 📝 Key Deliverables Checklist

### **Week 1-2:**
- [ ] Basic credit scoring model
- [ ] Feature engineering pipeline
- [ ] Model comparison notebook

### **Week 3-5:**
- [ ] PD/LGD/EAD models
- [ ] IFRS 9 staging implementation
- [ ] ECL calculator with scenarios

### **Week 6-8:**
- [ ] SHAP explainability report
- [ ] Model governance documentation (30+ pages)
- [ ] Stress testing framework

### **Week 9-12:**
- [ ] MLOps architecture design
- [ ] Data pipeline with DVC
- [ ] Drift monitoring dashboard
- [ ] Deployment pipeline

### **Week 13-15:**
- [ ] MCA feature engineering
- [ ] Segment-specific models
- [ ] Policy experiment framework
- [ ] Regulatory compliance documentation (50+ pages)

### **Week 16:**
- [ ] Complete credit risk system
- [ ] FastAPI decision service
- [ ] Executive dashboard
- [ ] System documentation (100+ pages)
- [ ] Live demonstration

---

## 📊 Success Metrics

| Phase | Metric | Target | Stretch |
|-------|--------|--------|----------|
| 1-2 | Model Gini | > 0.60 | > 0.65 |
| 3-5 | LGD R² | > 0.55 | > 0.60 |
| 5 | Feature PSI | < 0.10 | < 0.08 |
| 6-8 | Documentation | 90% complete | 100% complete |
| 9-12 | Monitoring Accuracy | 95% | 98% |
| 13-15 | Governance Alignment | 100% | 100% |
| 16 | System Readiness | Production-ready | Fully deployed |

---

## 🎓 Learning Philosophy

1. **Progressive Complexity:** Start with fundamentals, build to enterprise systems
2. **Hands-On Learning:** Code-first approach—read code, run code, modify code
3. **Production Focus:** All projects follow production best practices
4. **Governance First:** Model governance and auditability built in from start
5. **Regulatory Alignment:** All work maps to BSP/IFRS 9 requirements

---

## 🚀 Getting Started

### **Before Week 1:**
1. [ ] Clone all Tier 1 repositories
2. [ ] Set up Python environment (Python 3.10+)
3. [ ] Install key libraries: scikit-learn, pandas, jupyter, shap
4. [ ] Read TsoareloAdriaan11/IFRS9-ECL-ENGINE README
5. [ ] Skim Daniel11OSSE/ifrs9-ecl-modeling README
6. [ ] Bookmark key documentation links

### **Weekly Routine:**
- **Monday:** Review learning objectives, set up notebooks
- **Tuesday-Thursday:** Deep study, hands-on coding
- **Friday:** Complete deliverables, reflection
- **Weekend:** Consolidation, optional deep dives

---

## 📞 Support Resources

### **When Stuck:**
1. Check repository Issues & Discussions
2. Review related tutorial notebooks
3. Consult scikit-learn/SHAP documentation
4. Search Stack Overflow with specific error
5. Reach out to repository maintainers

### **Staying Current:**
- Watch GitHub repos for updates
- Follow KDnuggets & Towards Data Science
- Subscribe to BSP regulatory updates
- Join credit risk AI communities

---

## 🏁 Final Notes

This learning path is **designed specifically for your GoTyme role** and balances:
- Theoretical foundation (ML, statistics, finance)
- Practical implementation (production-ready code)
- Regulatory compliance (IFRS 9, BSP guidelines)
- Business application (MCA-specific credit risk)
- Governance & ethics (model explainability, auditability)

**Progress sequentially through all phases. Revisit repositories as you advance—each week builds on previous concepts.**

**Good luck! 🚀**

---

*Created August 30, 2026 for Senior Data Scientist Position at GoTyme MCA, South Africa*