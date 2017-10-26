# JIRA / VCS / CI comparison

# Common features
- Pull request management / code review in place
- Build and deploy on commit (easier with Bitbucket + Pipelines)
- Support custom manual job (vbump, manual deploy, etc...)
- Unlimited private repos

# Jira + Bitbucket + Bitbucket pipelines

### Pros
- Tight integration (We can use our Jira account)
- No third party involved for CI
- Permission management at branches level i.e: Only some users can push to `master`
- Integration where it matters in a project, at the repository level.
- CI docker as First Class citizen
    - Easy to spin up services, ideal for test integration(Java, nodejs, database, etc..)
- Pricing model
### Cons
- We have to configure pipelines
- Migrate repo
- All cloud / no server to maintains

### Pricing
- 2$ / user / month (500 build minutes included)
- 10$ / month for 1000 minutes

# Jira + Github Organization + Jenkins

### Pros
- Already setup
- Low monthly cost CI
### Cons
- No easy permission management(more difficult with private repo fork)
- Depends on a third party for CI
- CI maintenance
- Pricing model

### Pricing
- Jenkins: hosted on our server
- Github: 25$/month first five users + 9$ / user / month


# Pricing comparison

### Actual scenario
- (10 users) Guillaume, Jason, LP, Mark, Marcel, Maxime, PL, Robert, Sandrine, Tom
- max 1500 build minutes (~50 minutes / day)

### Total
- ***Jira + Github + Jenkins:*** 25$ + (5 users * 9$) = *70$ / month + 9$ / futur user*
- ***Jira + Bitbucket + Pipeline:*** 10 users * 2$ + 10$(1000 build minutes) = *30$ / month + 2$ futur user*