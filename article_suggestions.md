# Supplemental Articles & Case Studies — Day 10: CI/CD Part 2

**Deck:** `Day 10_CI _ CD Part 2.pptx`
**Purpose:** Real-world case studies + reference articles to make the deck's concepts stickier. Each entry notes which slides it reinforces and why.
**Recipient:** vicpal1989@gmail.com

---

## 1. Code Styling — PEP 8 (slide 2)

- **PEP 8 — Style Guide for Python Code (canonical source):** https://peps.python.org/pep-0008/
  Primary reference. Good to point students at the original text rather than a summary.
- **Mastering Python Code Quality: PEP 8, Pylint, and Black (Dinesh Suthar, Medium):** https://medium.com/@dineshsuthar03/mastering-python-code-quality-pep-8-pylint-and-black-69b71d945e7d
  Walks the PEP 8 → linter → formatter pipeline in one article — mirrors slides 2–4 almost exactly.

## 2. Linting (slide 3)

- **Pylint docs — "What is Pylint":** https://pylint.readthedocs.io/
  Bookmark for students who want to go beyond `pylint file.py`.
- **Python Auto Formatter: Autopep8 vs. Black (Built In):** https://builtin.com/data-science/autopep8-vs-black
  Useful companion — helps students understand *why* a team picks one tool over another.

## 3. Code Formatting — Black / isort / autopep8 (slide 4)

- **Consistent Python code with Black — Matt Layman:** https://www.mattlayman.com/blog/2018/python-code-black/
  Short practitioner narrative: "we adopted Black and here's what happened." Memorable because it frames Black as ending code-style bikeshedding.
- **Any Code Style You Like, So Long As It's Black — KI Labs Engineering:** https://medium.com/ki-labs-engineering/any-code-style-you-like-as-long-its-black-7a3cc4edd90
  Team-adoption case study from an engineering org. Pairs with slide 4's "opinionated formatter" point.
- **psf/black on GitHub (the "uncompromising formatter"):** https://github.com/psf/black

## 4. Deployment — general framing (slides 5–8)

- **Model Deployment Strategies (Neptune.ai):** https://neptune.ai/blog/model-deployment-strategies
  One-page survey of online/offline, batch, streaming, and progressive-rollout patterns. Great anchor article for the whole "Deployment" section.
- **Decoding Deployment in Machine Learning: Cases and Patterns (Medium):** https://medium.com/@kcsanjeeb091/decoding-deployment-in-machine-learning-cases-and-patterns-demystified-d215a19cfd83

## 5. Continuous Deployment vs. Continuous Delivery (slides 11–16)

- **Etsy DevOps Case Study: The Secret to 50+ Deploys a Day (Simform):** https://www.simform.com/blog/etsy-devops-case-study/
  The canonical CD case study. Concrete numbers (50 deploys/day, 6,419 deploys in a year) make the concept memorable.
- **How Etsy Deploys More Than 50 Times a Day (InfoQ):** https://www.infoq.com/news/2014/03/etsy-deploy-50-times-a-day/
  Shorter companion piece — good for a 5-minute read.
- **Continuous Deployment at Facebook and OANDA (IEEE paper):** https://ieeexplore.ieee.org/document/7883285/
  Academic, but the headline finding ("20× team size, 50× code size, no productivity loss") is a powerful soundbite.
- **Case Study: Continuous Delivery at Facebook (Rohan Gupta, Medium):** https://medium.com/@ThisRohanGupta/case-study-continuous-delivery-at-facebook-84b3a5f1b2e6
  Accessible summary of the IEEE paper.

## 6. Champion / Challenger (slides 15–16)

- **Implementing a Champion-Challenger ML System in Financial Services (Spatialedge):** https://www.spatialedge.ai/case-studies/implementing-a-champion-challenger-machine-learning-system-in-the-financial-services-sector
  Concrete case study: a South African insurer replacing actuarial models via continuous challenger testing. This is the exact pattern the slides describe.
- **Introducing MLOps Champion/Challenger Models (DataRobot):** https://www.datarobot.com/blog/introducing-mlops-champion-challenger-models/
- **Dynamic A/B Testing for ML Models with SageMaker MLOps (AWS):** https://aws.amazon.com/blogs/machine-learning/dynamic-a-b-testing-for-machine-learning-models-with-amazon-sagemaker-mlops-projects/

## 7. A/B Testing, Canary, Shadow (slides 17–22)

**Comparison / overview:**
- **Shadow Deployment vs. Canary Release of ML Models (JFrog ML / Qwak):** https://www.qwak.com/post/shadow-deployment-vs-canary-release-of-machine-learning-models
  Side-by-side comparison — maps 1:1 to slides 17–22.
- **Safely Deploying ML Models: A/B, Canary, Interleaved, Shadow (MarkTechPost, 2026):** https://www.marktechpost.com/2026/03/21/safely-deploying-ml-models-to-production-four-controlled-strategies-a-b-canary-interleaved-shadow-testing/

**Canary specifically:**
- **Google SRE Workbook — Canarying Releases:** https://sre.google/workbook/canarying-releases/
  The definitive "how Google does it" chapter. Memorable framing: the canary as an "early-warning system."
- **Canary Deployments and A/B Testing — Safer, Smarter Model Rollouts (Medium):** https://medium.com/@sebuzdugan/day-60-100-canary-deployments-and-a-b-testing-safer-smarter-model-rollouts-d9245042baf9

**Shadow specifically:**
- **Minimize Production Impact of ML Model Updates with SageMaker Shadow Testing (AWS):** https://aws.amazon.com/blogs/machine-learning/minimize-the-production-impact-of-ml-model-updates-with-amazon-sagemaker-shadow-testing/
  AWS engineering blog — strong real-world case study with latency/error-rate metrics.
- **Deploying ML Models in Shadow Mode (Christopher Samiullah):** https://christophergs.com/machine%20learning/2019/03/30/deploying-machine-learning-applications-in-shadow-mode/
  Practitioner tutorial, less marketing, more code.

## 8. Blue-Green Deployment (slides 23–24)

- **Real-World Blue-Green Deployment: 10 Lessons I Wish I Knew Earlier (dev.to):** https://dev.to/egor_kaleynik_7dbe9393e86/real-world-blue-green-deployment-10-lessons-i-wish-i-knew-earlier-71j
  Opinionated "war stories" post — the lesson about DNS taking 83 minutes to propagate in Southeast Asia is the kind of detail students remember.
- **Database Reliability Engineering: AWS RDS Blue/Green Deployments at Arcadia (purdy.dev):** https://www.purdy.dev/words/2024/01/blue-green-deployments-at-arcadia/
  Real SRE case study — applies the pattern to *databases*, which is usually where blue-green gets hardest.
- **How Blue-Green Deployments Work in Practice (Earthly):** https://earthly.dev/blog/blue-green/

## 9. Feature Flags / Application-based Release (slide 25)

- **Modernizing Development & Controlling Rollout with Feature Flags — case study (LaunchDarkly):** https://launchdarkly.com/blog/case-study-modernizing-development-controlling-rollout-with-launchdarkly/
- **Animoto Delivers Software 3× Faster with LaunchDarkly:** https://launchdarkly.com/case-studies/animoto/
  Concrete win: idea-to-prod time dropped from 3 weeks → 1 week.
- **Feature Flags: Beyond the Boolean (LaunchDarkly):** https://launchdarkly.com/blog/feature-flags-beyond-the-boolean/
  Good complement to slide 25's "combine with canary" bullet.

## 10. Git Branching Strategies (slides 26–40)

- **Trunk-Based Development (official site, Paul Hammant):** https://trunkbaseddevelopment.com/
  The reference site. Includes the memorable stat: **Google runs trunk-based dev with ~35,000 developers in a single monorepo.**
- **Trunk-Based Development vs. Git Flow (Toptal):** https://www.toptal.com/software/trunk-based-development-git-flow
- **Gitflow Workflow (Atlassian):** https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow
  The canonical GitFlow diagram lives here — good to cross-reference with slide 40.
- **Atlassian — Trunk-Based Development:** https://www.atlassian.com/continuous-delivery/continuous-integration/trunk-based-development
- **Git Branching Strategies vs. Trunk-Based Development (LaunchDarkly):** https://launchdarkly.com/blog/git-branching-strategies-vs-trunk-based-development/
  Ties branching choices back to feature flags — bridges slides 25 and 37–40 nicely.

---

## Suggested "pair one article per slide group" shortlist

If you want to assign just *one* link per concept, these are the most memorable picks:

| Concept | One-link pick |
|---|---|
| PEP 8 / linting / Black | https://medium.com/@dineshsuthar03/mastering-python-code-quality-pep-8-pylint-and-black-69b71d945e7d |
| Continuous deployment | https://www.simform.com/blog/etsy-devops-case-study/ |
| Champion / challenger | https://www.spatialedge.ai/case-studies/implementing-a-champion-challenger-machine-learning-system-in-the-financial-services-sector |
| Canary | https://sre.google/workbook/canarying-releases/ |
| Shadow | https://aws.amazon.com/blogs/machine-learning/minimize-the-production-impact-of-ml-model-updates-with-amazon-sagemaker-shadow-testing/ |
| Blue-green | https://dev.to/egor_kaleynik_7dbe9393e86/real-world-blue-green-deployment-10-lessons-i-wish-i-knew-earlier-71j |
| Feature flags | https://launchdarkly.com/case-studies/animoto/ |
| Branching strategies | https://trunkbaseddevelopment.com/ |
