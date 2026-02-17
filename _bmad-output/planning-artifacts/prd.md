---
stepsCompleted: ["step-01-init", "step-02-discovery", "step-02b-vision", "step-02c-executive-summary", "step-03-success", "step-04-journeys", "step-05-domain", "step-06-innovation", "step-07-project-type", "step-08-scoping", "step-09-functional", "step-10-nonfunctional", "step-11-polish"]
inputDocuments:
  - _bmad-output/planning-artifacts/product-brief-doortogate-2026-02-17.md
  - _bmad-output/planning-artifacts/research/market-travel-visibility-anxiety-reduction-competitor-landscape-research-2026-02-17.md
  - docs/mockups/option-1.html
workflowType: 'prd'
projectType: 'greenfield'
briefCount: 1
researchCount: 1
projectDocsCount: 1
date: 2026-02-17
author: Ben
classification:
  projectType: "web_app"
  domain: "travel_transportation"
  complexity: "medium"
  projectContext: "greenfield"
---

# Product Requirements Document - doortogate

**Author:** Ben
**Date:** 2026-02-17

## Executive Summary

**Door-to-Gate Pulse** is a Progressive Web App that eliminates travel anxiety for occasional airline travelers by providing a unified, real-time confidence score for their entire journey from home to departure gate. The app aggregates traffic data, TSA wait times, flight status, incoming aircraft tracking, weather impacts, and community-driven updates into a single dashboard with one critical metric: percentage confidence of on-time gate arrival.

**Target Users:** Occasional travelers with families (3-4 trips/year) — specifically the "anxious planners" who compensate for uncertainty by obsessively checking multiple fragmented apps, arriving 3+ hours early, and creating stress for their travel companions. Sarah, the primary persona, is a 38-year-old marketing manager and mother of two who nearly missed a flight three years ago and has developed significant travel anxiety.

**Core Problem:** These travelers face decision paralysis from fragmented information (Google Maps, FlightAware, TSA websites, airline apps, weather apps) requiring constant mental math and recalculation. No existing solution answers the fundamental question: "Am I going to make it on time?" This leads to unhealthy stress, relationship strain with family members, wasted time (arriving 3+ hours early), and diminished travel experiences.

**Solution Approach:** A confidence algorithm combines drive time (weighted 35%), TSA wait (70%), weather impact (120%), and flight status into a single 0-100% confidence score with color-coded thresholds (green 80%+, yellow 60-79%, red <60%). Real-time recalculation (< 500ms) and push notifications alert users when conditions change. Built as Next.js PWA, installable on iPhone without app store friction, hosted on Vercel with < 2 second load times on 4G.

### What Makes This Special

**Confidence-Orchestrator Positioning:** Incumbents are strong but siloed (maps, flight tracking, itinerary, booking). Door-to-Gate is positioned as a cross-silo confidence orchestrator for anxious occasional travelers, converting fragmented operational signals into one trusted "leave now / hold" decision.

**Anxiety-Reducing UX:** Interface and confidence algorithm specifically designed to reduce anxiety by providing permission to relax, not just more data. The holistic view with single confidence score eliminates mental burden of constant recalculation across fragmented sources.

**Community Network Effect:** Waze-style crowdsourced updates create network effect where more users generate better real-time data, making the platform increasingly valuable and difficult to replicate. Community TSA reports, traffic delays, and gate changes automatically update confidence scores for all users.

**Occasional Traveler Focus:** Designed for anxious travelers who fly 3-4 times/year for family vacations, not seasoned road warriors. No assumptions of travel expertise or familiarity — UX optimized for anxiety reduction and trust-building within first 3 uses.

**PWA Strategic Advantage:** Eliminates app store friction, maximizing accessibility for occasional travelers who resist downloading "another app." Installable directly from web with full notification capabilities for time-sensitive alerts.

**AI-Ready Foundation:** Architecture designed to evolve with AI capabilities for predictive recommendations, personalized anxiety triggers, intelligent alert optimization, and pattern learning (user's typical drive times, preferred time buffers).

## Project Classification

**Project Type:** Web App (Progressive Web App)  
**Domain:** Travel/Transportation Technology  
**Complexity:** Medium — Multiple real-time API integrations (traffic, flight tracking, weather, TSA), community platform with data aggregation, confidence algorithm with weighted calculations, real-time updates with < 5 second latency, but not heavily regulated like healthcare or fintech  
**Project Context:** Greenfield (new product from scratch)  
**Technical Stack:** Next.js, Vercel hosting, PWA manifest for iPhone installation  
**Critical Integrations:** Google Maps/Mapbox (traffic), FlightAware/AviationStack (flight tracking), OpenWeatherMap + turbli.com (weather/turbulence), MyTSA API + community-driven (TSA wait times)

## Success Criteria

### User Success

**Primary Goal: Reduce Travel Anxiety and Build Trust**

**Behavioral Success Indicators:**
- **App Becomes Single Source of Truth:** 80% of users report checking only Door-to-Gate Pulse during active travel monitoring (vs. checking 4-5 fragmented apps)
- **Cross-Check Reduction:** 60%+ of users reduce cross-checking of 3+ external apps by their second tracked trip
- **Trust Development:** 70% of users report "trusting the app's confidence score" within first 3 uses; users act on app recommendations without second-guessing
- **Recommendation Acceptance:** 65%+ acceptance rate for "leave now" recommendations within first 90 days
- **Optimized Departure Timing:** Average airport arrival time moves from 180 minutes to 90 minutes before flight (60-90 minute optimal window)
- **Reduced Family Stress:** 75% of users report "less stressful travel day" after using app; travel companions validate improved experience
- **Engagement & Retention:** 85% retention rate for users with 2+ trips per year; 60% PWA installation rate

**Success Moment Validation:**
- **"Aha!" Moment:** 80% of users complete first full journey (home to gate) within 2 weeks of signup
- **User realizes trust:** First time confidence score drops from 87% to 74% with alert "TSA wait increased - consider leaving 10 mins earlier" and user acts on it without second-guessing
- **Emotional Success:** Sarah sees "84% confidence" and can relax for 20 more minutes instead of asking "should we leave now?" every 10 minutes

### Business Success

**3-Month Success Criteria (MVP Launch):**
- 5,000+ active users across 3-5 major airports
- Net Promoter Score (NPS) > 40 indicating strong product-market fit
- 50+ daily community contributions (TSA wait times, gate updates, traffic reports)
- 15% of active users contribute at least one report per trip
- Confidence algorithm accuracy: 85%+ (prediction vs. actual outcome)
- API integrations stable with 99%+ uptime
- PWA installation and notification system working seamlessly

**12-Month Success Criteria (Growth Phase):**
- 100,000+ registered users
- Coverage expansion to top 25 US airports
- Organic growth rate of 15-20% month-over-month via referrals
- 25% of active users contributing community reports
- Community data improving confidence algorithm accuracy to 90%+
- Average report freshness under 15 minutes during peak travel times
- DAU/MAU ratio > 30% during travel seasons
- 90% retention rate for users with 2+ trips per year

### Technical Success

**Core Functionality Performance:**
- Confidence algorithm accuracy: 85%+ at launch → 90%+ by month 12
- App load time: < 2 seconds on 4G connection
- Confidence score calculation time: < 500ms
- Real-time update latency: < 5 seconds for community reports
- API uptime: 99.5%+ for all critical integrations
- Push notification delivery: 95%+ success rate
- Error rate: < 0.5% of user sessions
- False-alert rate: < 10% for "leave now" recommendations
- Missed-critical-alert rate: < 2% for material disruption events within monitored window

**Integration Stability:**
- All 4 critical data sources (traffic, flight, weather, TSA) operational
- Graceful degradation when one source fails (app remains functional)
- Real-time updates working with < 5 second latency

**PWA Performance:**
- Installable on iPhone with single-tap from browser
- Offline mode works for viewing cached flight data
- Push notifications deliver with < 5 second delay for time-sensitive alerts

### Measurable Outcomes

**User Adoption KPIs:**
- Trip completion rate: 80% of users complete full journey tracking (home to gate)
- PWA installation rate: 60%+ (vs. browser-only use)
- Average sessions per trip: 8-12 sessions (pre-travel through gate arrival)
- Community contribution rate: 15% (month 3) → 25% (month 12)
- Referral rate: 30% of users refer at least one friend/family member

**User Success KPIs:**
- User-reported anxiety reduction: 75% report "less stressful travel"
- NPS: 40+ (month 3) → 60+ (month 12)
- 30-day retention: 70%+ (users return for next trip)
- Trip-to-trip retention: 85%+ (users with 2+ trips per year)

**Community Health KPIs:**
- Report freshness: Average age < 30 minutes (month 3) → < 15 minutes (month 12)
- Airport distribution: Reports distributed across 10+ airports (month 3) → 25+ airports (month 12)
- Community validation: TSA reports match actual wait times within 20% margin

## Product Scope

### MVP - Minimum Viable Product

**Must Have for Launch:**

**1. Unified Confidence Dashboard**
- Flight entry by flight number with auto-population (departure time, gate, airline, destination)
- Automatic home location detection via GPS (user can override)
- Real-time confidence score: 0-100% with color-coded indicator (green 80%+, yellow 60-79%, red <60%)
- Explainability panel: "Why confidence changed" with top contributing factors
- Comprehensive data display: Drive/GPS time, TSA wait, flight status, incoming aircraft, weather impact
- Source freshness timestamps for each data card and score update
- Uncertainty indicator when one or more sources are stale/partial
- All data consolidated in single scrollable dashboard matching mockup UX

**2. Critical Data Integrations**
- Traffic & Navigation: Google Maps API or Mapbox for real-time drive times with traffic
- Flight Tracking: FlightAware API or AviationStack for flight status and incoming aircraft tracking
- Weather Data: OpenWeatherMap + turbli.com for weather/turbulence forecasts
- TSA Wait Times: Community-driven (primary) + MyTSA API if available (supplementary)

**3. Community Feedback Network (Simplified)**
- Basic report submission: Select type (TSA Wait, Traffic Delay, Gate Status), enter value, optional user handle
- Community reports display: Live table showing recent reports (last 2 hours) with auto-refresh every 30 seconds
- Data integration: Community reports automatically update confidence score

**4. PWA Essentials**
- Installable on iPhone home screen with PWA manifest
- Push notifications: "Time to leave in X minutes", confidence drop alerts, gate changes, flight delays
- Fast load times (< 2 seconds on 4G)
- Works offline for viewing cached flight data
- Mobile-first responsive design matching mockup

**5. Confidence Algorithm**
- Weighted calculation: TSA wait (highest weight), traffic (second), weather (third)
- Real-time recalculation on data updates (< 500ms)
- Alert thresholds trigger notifications on significant changes
- Degraded-mode behavior when sources fail, including transparent fallback messaging

**6. Phased Airport Coverage**
- Phase 1 (MVP): Top 20 US airports by passenger volume
- Phase 2: Expand to top 50 airports after data quality thresholds are met
- Phase 3: Roll out to all commercial US airports with scheduled passenger service
- Airport database (IATA codes, locations, terminals)
- Checkpoint mapping for major airports (top 50); generic "TSA Security" for smaller airports
- Community contributions fill in specific checkpoint details over time

**Not in MVP:**
- User accounts/authentication (optional handle only for community reports)
- Quick action buttons ("TSA Improving", "Traffic Slowing", etc.)
- Upvoting/downvoting reports for credibility
- Multi-user/family coordination features
- Payment/monetization
- Advanced personalization (historical pattern learning)
- International flights

### Growth Features (Post-MVP)

**Version 2.0 (6-12 Months Post-MVP):**

**Enhanced Community Features:**
- Quick action buttons for rapid reporting
- Report credibility system (upvotes, user reputation)
- Community leaderboards (gamification for contributors)
- Photo attachments for gate changes or conditions
- Real-time community chat for travelers on same flight

**Multi-User/Family Coordination:**
- Share trip with travel companions
- Coordinated departure timing ("everyone ready in 10 mins")
- Family notifications and check-ins
- Group confidence score accounting for multiple pickup locations

**Personalization & AI:**
- Learn user patterns (typical drive times, preferred buffers)
- Personalized anxiety threshold settings
- AI-powered recommendations: "Based on your history, leave in 12 minutes"
- Custom alert preferences (only notify if confidence drops below threshold)

**User Accounts:**
- Optional account creation for cross-device sync
- Trip history and analytics
- Saved home locations and preferences
- Community reputation tracking

### Vision (Future)

**Version 3.0 (12-24 Months):**

**International Expansion:**
- Support international flights and airports globally
- Customs/immigration time estimates
- Global community network
- Multi-language support

**Deep Integration Ecosystem:**
- Airport parking booking with real-time availability
- Rideshare pre-booking with optimal departure timing
- TSA PreCheck/Clear integration for faster checkpoint routing
- Airline partnerships for enhanced data access
- Travel insurance offers based on real-time risk factors

**Advanced Features:**
- Connection flight support (multi-leg journey optimization)
- Airport terminal maps and navigation
- Gate proximity alerts ("start walking to gate in 5 mins")
- Post-trip analytics and pattern learning

**Monetization Evolution:**
Monetization optimization is deferred until trust and retention thresholds are met (confidence trust, recommendation acceptance, and trip-to-trip retention KPIs).
- Freemium model: Premium features for $4.99/month
- Partnership revenue (parking, rideshare, insurance affiliates)
- Airline B2B licensing of confidence algorithm
- Light advertising (airport lounges, pre-travel services) with strict policy: no ads during active travel monitoring

**Platform Vision (2-3 Years):**
- Expand beyond airports: train stations, cruise terminals, major events
- B2B licensing to travel companies and airlines
- API platform for third-party integrations
- White-label solutions for airports and airlines
- AI-powered travel assistant with proactive recommendations
- Voice assistant integration ("Alexa, am I on time for my flight?")
- Community platform: traveler social network, travel tips database, real-time airport condition reports

**Long-Term North Star:** Door-to-Gate Pulse becomes the trusted source for travel timing intelligence—the app anxious travelers open first and trust completely, eliminating travel anxiety for millions of occasional flyers and creating a vibrant community of travelers helping each other navigate air travel complexities.

## User Journeys

### Journey 1: Sarah's Anxiety-to-Confidence Transformation (Primary User - Core Happy Path)

**Opening Scene: The Night Before**

Sarah, 38-year-old marketing manager and mother of two, sits at her kitchen table at 9 PM the night before a family trip to visit her parents in Phoenix. She opens her laptop and starts her usual ritual: creates a spreadsheet with departure calculations, checks Google Maps for tomorrow's drive time (32 minutes currently), visits the airline website to confirm the 6:45 PM flight, and searches "Sky Harbor TSA wait times" only to find a website last updated three days ago showing "15-25 minutes."

Her stomach tightens. Three years ago, a gate change she didn't catch almost made them miss their Disney flight. Her kids cried, her husband was frustrated, and she's been hyper-vigilant ever since. Tonight, she calculates they should leave by 3:00 PM "just to be safe" — a full 3 hours and 45 minutes before departure.

Her friend mentioned Door-to-Gate Pulse last week: "This app saved our Disney trip!" Sarah downloads it, enters flight FR 2419, and sees the dashboard appear instantly.

**Rising Action: The Power of One Number**

The screen shows "84% chance on-time gate arrival" in reassuring green. Below it, a clean dashboard displays everything she was frantically checking across five different sources:
- Drive/GPS: 32 min (moderate traffic)
- TSA Wait: 18 min (Checkpoint C2, reported 6 mins ago by @MiaR)
- Flight Status: On time, Gate B18, boarding 6:10 PM
- Incoming Aircraft: N381FR from SFO, 43 mi out, expected at gate 5:58 PM
- Weather Impact: 14% (rain bands north of field until 6:20 PM)

For the first time in three years, Sarah exhales. One number. One screen. Everything she needs.

She enables notifications and sets it aside. Her daughter Emma asks if they can stop at the craft store tomorrow before the airport. Normally Sarah would snap "absolutely not!" But tonight, seeing that 84% confidence and knowing she'll get an alert if conditions change, she says "maybe — let's check the app tomorrow."

**The Next Day: Trust Building**

At 2 PM, Sarah opens the app. Still 84% confidence. "Time to leave: 3 hours 25 minutes." She can relax.

At 3:15 PM, she checks again. The confidence dropped to 74%. Her heart races — this is what she feared! But the notification explains: "TSA wait increased to 24 mins (up from 18). Consider leaving 10 mins earlier." 

This is the moment. Sarah tells David "the app says we should leave in 15 minutes instead of 20." He shows her the screen. David can see the data too. No argument. No "are you sure?" They leave at 3:30 PM instead of her original 3:00 PM panic departure.

**Climax: The Confidence Pays Off**

In the car, Sarah quickly reports "Traffic on I-10 backed up near exit 147" at a red light. The app absorbs her contribution and updates. She checks incoming aircraft status — still on track for 5:58 PM arrival.

At the airport, checkpoint C2 has a line. Sarah feels her anxiety spike, but she sees a community update from 3 minutes ago: "@TravelDad21 - PreCheck moving fast, regular C2 slow, try C3." They walk to C3, breeze through in 12 minutes. Sarah submits "Checkpoint C3 - 12 mins actual."

**Resolution: The New Reality**

They arrive at Gate B18 at 5:50 PM — perfect timing. Not 3 hours early. Not stressed. Emma got to stop at the craft store. David didn't endure 30 "should we leave now?" questions. Sarah's parents video-call to say hi before the flight, and Sarah is actually smiling and relaxed instead of frazzled.

The app shows "94% confidence - you made it!" Sarah thinks: "I need this for every trip."

**Journey Requirements:**
- Flight entry with instant auto-population of flight details
- Real-time confidence algorithm with color-coded thresholds
- Unified dashboard consolidating all data sources (no app-switching)
- Push notifications with specific actionable guidance ("leave 10 mins earlier")
- Community contribution system with simple submission
- Real-time community updates visible to all users on same route
- GPS location detection for drive time calculations
- Notification permission prompts for time-sensitive alerts

---

### Journey 2: Mike's Power Contributor Experience (Secondary User - Community Builder)

**Opening Scene: The Frequent Flyer**

Mike, 45-year-old sales director, travels 2-3x monthly for work. He's mastered the airport game: TSA PreCheck lane C moves fastest at Sky Harbor between 4-6 PM, Gate B terminal has the best coffee, he knows which parking structures fill up first. When traveling solo for work, he's efficient and stress-free.

But this Friday, his wife and teenage daughter join him for a long weekend in San Diego. Suddenly he's responsible for getting everyone there smoothly. His wife asks "what time should we leave?" and Mike realizes his internal knowledge isn't enough — he needs real-time data they can all trust.

A colleague mentioned Door-to-Gate Pulse: "It's like Waze for airports, and people like you would love contributing." Mike downloads it, enters their flight, and immediately sees the value: one screen, one confidence score, community-driven updates.

**Rising Action: Contributing Pro Tips**

Mike checks the app Thursday night: 87% confidence, TSA PreCheck lane C showing 8 minutes. Perfect. He enables notifications and feels confident.

Friday afternoon at the airport, Mike's wife and daughter are with him at PreCheck. He notices lane C moving exceptionally fast today — they clear in 6 minutes. While walking to the gate, Mike opens the app and taps "Submit Report." He selects "TSA Wait," types "6 mins," enters "@MikeFlys" as his handle, and submits "TSA PreCheck lane C moving fast - 6 mins."

He feels good knowing other families behind him will benefit from his real-time intel.

**Climax: The Community Value Loop**

At the gate waiting for boarding, Mike sees his update in the community feed. Within 2 minutes, someone else confirms: "@SarahT - Can confirm, PreCheck C super fast right now!" The app's confidence score for users approaching the airport adjusts upward slightly.

Mike's daughter rolls her eyes good-naturedly: "Dad's showing off his travel skills again." But his wife smiles and says "this is actually really helpful — I feel way less stressed than usual."

**Resolution: Becoming an Advocate**

On the return flight Sunday, Mike uses the app again. He reports when their parking structure is full, when Gate B22 changes to B18, when a weather delay adds 15 minutes. Each contribution takes 10 seconds. Each one helps travelers behind him.

Monday, back in the office, a colleague mentions travel stress. Mike says "I know the airport game. Download this app — you share what you see, you get intel from others. Everyone wins." He's referred three people within a week.

**Journey Requirements:**
- Quick, frictionless report submission (< 10 seconds)
- Optional user handle system (no required authentication)
- Community feed displaying recent reports with timestamps
- Real-time propagation of community reports to other users
- Visible confirmation that contribution was received (appears in feed)
- Multiple report types (TSA Wait, Traffic, Gate Status)
- Simple form interface (dropdown + text field)

---

### Journey 3: David's Indirect Benefit (Secondary User - Travel Companion)

**Opening Scene: The Reluctant Navigator**

David, 40-year-old engineer and Sarah's husband, has learned to avoid travel-day conflict. When Sarah asks "should we leave now?" for the fifth time, he just nods. When she insists they leave at 3:00 PM for a 6:45 PM flight, he doesn't argue — it's not worth it.

But last night, Sarah showed him an app: "Look, it says 84% confidence. We're okay to leave at 3:30 PM." David is skeptical. Sarah's tried other apps before and still asked him repeatedly. But he sees the unified dashboard and thinks "maybe this will help."

**Rising Action: The Shared Truth Source**

Friday at 3:15 PM, Sarah says "the app says leave in 15 minutes. Traffic increased." David expects the usual "but are you sure?" conversation. Instead, Sarah shows him her phone. He can see the same data. The confidence score dropped to 74% with a specific alert about TSA timing.

For the first time in their marriage, there's no debate. No repeated questions. One notification: "Leave in 15 minutes." They leave at 3:30 PM.

**Climax: The Peaceful Drive**

In the car, David expects Sarah to check and recheck everything. But she just looks at the app once, says "we're good," and puts her phone away. They actually talk about the weekend plans instead of "how's the traffic" and "what if we're late."

Emma in the back seat is listening to music, relaxed. Normally by now, Sarah would have mentioned the flight three times. Today, silence. Peaceful silence.

**Resolution: Getting His Wife Back**

They arrive at the gate with time to spare. Sarah is calm. She's not frantically checking her phone. She's present. Emma says "Mom, can we get Starbucks?" and Sarah says "yes" without checking the time five times first.

David thinks: "If Sarah has an app she trusts, I get my wife back for the actual vacation." He doesn't use the app himself, but he benefits immensely when Sarah does.

**Journey Requirements:**
- Sharable confidence score (visual display easy to show others)
- Clear, simple notifications that both partners can trust
- No required user account or authentication for viewing
- Confidence score visible at a glance
- Specific, actionable alerts that reduce debate between travel partners

---

### Journey 4: Operations/Monitoring User (Admin Perspective - Future Consideration)

**Opening Scene: Platform Health Monitoring**

Jennifer, product operations lead for Door-to-Gate Pulse, starts her Monday morning by checking platform health. She needs to ensure:
- API integrations are operational (FlightAware, Google Maps, OpenWeatherMap, turbli.com)
- Community reports are flowing (target: 50+ daily contributions)
- Confidence algorithm accuracy is tracking (target: 85%+)
- No user-reported issues with notifications or data quality

**Rising Action: Data Quality Investigation**

Jennifer notices Sky Harbor's TSA wait time reports dropped significantly over the weekend — only 12 reports across all checkpoints vs. usual 40+. She investigates:
- Checks if community contribution feature is working (yes)
- Looks at user volumes (normal)
- Examines airport-specific patterns (holiday weekend, lower traffic)

She correlates with actual user outcomes: confidence predictions for Sky Harbor users still 87% accurate despite lower community data volume. Historical patterns are filling gaps effectively.

**Climax: Proactive Issue Resolution**

Jennifer sees a spike in error logs for Atlanta airport flight tracking API calls. FlightAware integration appears degraded. She:
- Checks graceful degradation working correctly (yes, app shifts to AviationStack backup)
- Confirms users still receiving flight status updates
- Files ticket with FlightAware support
- Monitors user impact metrics (minimal degradation)

**Resolution: Platform Resilience Validated**

By end of day, FlightAware integration restored. Zero user complaints during the outage — graceful degradation worked perfectly. Jennifer documents the incident and confirms architectural resilience assumptions.

She prepares weekly report showing 89% confidence algorithm accuracy, 5,200 active users (up from 5,000), 62 daily community contributions (above target), 99.3% API uptime across all services.

**Journey Requirements (Future V2):**
- Operations dashboard with platform health metrics
- API integration monitoring and alerts
- Community contribution tracking by airport/type
- Confidence algorithm accuracy tracking
- User impact metrics during degraded states
- Incident logging and resolution tracking
- Weekly/monthly reporting capabilities

---

### Journey Requirements Summary

**From Sarah's Journey (Primary User - Core Experience):**
- Flight entry with flight number auto-population
- Real-time confidence score algorithm (0-100%, color-coded)
- Unified data dashboard (traffic, TSA, flight, weather, incoming aircraft)
- Push notifications with actionable guidance
- Simple community report submission
- GPS location detection for drive time
- Real-time data refresh (< 5 second latency)

**From Mike's Journey (Power Contributor):**
- Frictionless report submission (< 10 seconds)
- Optional user handle system (no auth required)
- Community feed display with timestamps
- Multiple report types (TSA, Traffic, Gate)
- Visible contribution confirmation
- Real-time report propagation to other users

**From David's Journey (Travel Companion):**
- Shareable confidence score display
- No authentication required for viewing
- Clear, simple notification format
- Confidence score visible at a glance
- Trust-building UX (reduce debate between partners)

**From Jennifer's Journey (Operations - V2):**
- Operations dashboard for platform health
- API integration monitoring
- Community contribution metrics
- Confidence algorithm accuracy tracking
- Incident and degradation management
- Reporting capabilities

**Core Capabilities Revealed:**
1. **Confidence Engine:** Real-time algorithm combining multiple data sources with weighted calculations
2. **Data Aggregation:** Flight tracking, traffic/GPS, weather, TSA wait times, community reports
3. **Notification System:** Time-sensitive push alerts with specific actionable guidance
4. **Community Platform:** Report submission, display, propagation, and integration into confidence calculations
5. **PWA Infrastructure:** Installable, offline-capable, notification permissions
6. **Monitoring & Operations (V2):** Platform health, API monitoring, metrics tracking

## Innovation & Novel Patterns

### Detected Innovation Areas

**Confidence-Orchestrator Architecture:**
Door-to-Gate Pulse unifies traffic (Google Maps/Mapbox), TSA wait times (community + MyTSA API), flight status (FlightAware/AviationStack), incoming aircraft tracking, weather impact (OpenWeatherMap), turbulence forecasts (turbli.com), and community reports into a single confidence algorithm. Existing solutions force travelers to mentally synthesize data across 4-6 fragmented apps.

**Anxiety-Centered Design Philosophy:**
Unlike data-first competitors (FlightAware, FlightStats), the entire UX optimizes for anxiety reduction through decisional clarity. The confidence score provides permission to relax or permission to leave early — answering "Am I going to make it?" rather than presenting raw data for user interpretation. Color-coded thresholds (green 80%+, yellow 60-79%, red <60%) bypass cognitive load.

**Community Network Effect as Moat:**
Waze-style crowdsourced TSA waits, traffic delays, and gate changes create increasing-returns network effect where more users generate better real-time data. Early market entry allows community-building before competitors can replicate the data quality, creating defensible moat beyond technology.

**PWA Strategy for Occasional Travelers:**
First travel confidence product using PWA to eliminate app store friction. Critical innovation for target user (Sarah: 3-4 trips/year) who resists downloading "another app" but will install from web during pre-trip anxiety spike. Competitors locked into app store distribution lose 80% of occasional travelers at download friction point.

**V2 AI-Ready Architecture:**
Foundation designed for AI evolution: predictive recommendations based on user patterns, personalized anxiety trigger learning, intelligent alert optimization (when to notify based on user's typical buffer preferences), and pattern recognition across community data for anomaly detection.

### Market Context & Competitive Landscape

**Why Now:** Convergence of real-time API availability (Google Maps traffic, TSA wait time APIs, flight tracking APIs), PWA maturity for notification capabilities, proven community-sourcing models (Waze, Gasbuddy), and market gap in anxiety-focused travel tools creates unique timing window.

**Competitive Moats:**
- Data aggregation relationships (API partnerships) require 6-12 months to establish
- Community network effect compounds monthly (100 users → 1000 users = 10x data quality, not 10x cost)
- PWA installation flow optimized for anxiety-driven adoption (2-click install vs app store friction)
- Confidence algorithm weights refined through user feedback (proprietary learning)

**Adjacent Competition:**
- TripIt (itinerary management, no real-time confidence scoring)
- FlightAware (flight-only, no door-to-gate coverage)
- Google Maps (drive time only, no travel context)
- Airline apps (post-security only, no pre-arrival planning)
- KAYAK Trips, Wanderlog, Tripsy (travel planning and itinerary workflow ownership)
- Polarsteps, Roadtrippers, Rome2Rio, Omio (planning habit and multi-leg journey orchestration)

None combine full journey or optimize for anxiety reduction.

**Competitor Benchmark (Consumer Apps):**
| Competitor | Release Timing | Market Proxy | Gap vs Door-to-Gate |
|---|---|---|---|
| Google Maps | 2005 | 2B+ monthly users | Strong ground ETA, weak door-to-gate confidence orchestration |
| FlightAware | 2005 | 12M+ passenger users | Strong flight status, weak pre-airport decision confidence |
| Flightradar24 | 2006 | 5M+ daily users, 100M+ downloads | Strong flight visibility, limited travel-day orchestration |
| TripIt | 2006 | 22M+ travelers | Strong itinerary organization, limited real-time confidence actions |
| Hopper | 2007 (app growth era ~2015+) | 120M+ downloads | Strong booking economics, not anxiety-reduction timing orchestration |
| Flighty | 2019 | Millions of users | Strong flight UX, limited full journey orchestration |

**Tiered Competitor Map (Expanded via "Travel Planning Apps"):**
- **Tier 1 - Direct Adjacent (high overlap):** Google Maps, FlightAware, Flightradar24, TripIt, Flighty
- **Tier 2 - Planning Workflow Competitors:** KAYAK Trips, Wanderlog, Tripsy
- **Tier 3 - Multi-Modal/Route Planning Competitors:** Roadtrippers, Rome2Rio, Omio, Polarsteps
- **Strategic Implication:** We do not need to beat every feature in Tier 2/3. We need to win the "travel-day confidence decision" wedge with trust, timeliness, and explainability.

### Validation Approach

### Assumptions and Validation

**Assumption 1: Users prefer decision confidence over raw data breadth**
- Experiment: A/B test score-first dashboard vs multi-card detail-first dashboard
- Pass Threshold: score-first cohort shows +20% recommendation acceptance with no increase in missed-critical-alert rate

**Assumption 2: First successful trip is the retention hinge**
- Experiment: track first-trip completion outcome vs 30/90-day retention
- Pass Threshold: users with first-trip success retain at least 2.5x better than first-trip failure cohort

**Assumption 3: Social proof materially improves adoption**
- Experiment: add high-quality social proof (recent testimonials, usage counters, review snippets) to onboarding and app store copy
- Pass Threshold: +15% install/start rate lift and +10% completion of first monitored trip

**Phase 1: Algorithm Accuracy (Months 1-3)**
- Target: 85% prediction accuracy (user arrives with 15+ minutes gate buffer when confidence >80%)
- Method: Track 500 user journeys end-to-end, measure actual vs predicted arrival times
- Success metric: <15% of green-confidence users report late gate arrival

**Phase 2: Anxiety Reduction (Months 1-6)**
- Target: NPS 40+ by Month 3, 50+ by Month 6, 60+ by Month 12
- Method: Post-trip surveys asking "Did Door-to-Gate Pulse reduce your travel stress?" (5-point scale)
- Behavioral validation: Track early arrival reduction (average 180 minutes pre-app → 120 minutes post-app for anxious users)

**Phase 3: Community Network Effect (Months 3-12)**
- Target: 30% of users submit ≥1 community report per trip by Month 6
- Method: Track community contribution rates, data freshness (<5 min for TSA waits in top 20 airports)
- Validation: Compare algorithm accuracy with vs without community data (target 10% improvement)

**Phase 4: PWA Adoption (Ongoing)**
- Target: 60% install-to-web-visit ratio for users with <7 days to departure
- Method: Track installation funnel, identify friction points
- Validation: Compare retention: installed PWA users vs web-only users (target 3x retention)

### Risk Mitigation

**Risk 1: API Reliability Failures**
- **Scenario:** FlightAware API downtime during peak travel (Thanksgiving)
- **Mitigation:** Fallback to secondary APIs (AviationStack), graceful degradation with cached data, transparent communication ("Flight data temporarily unavailable, using last update from 5 min ago")
- **Threshold:** Design for 99.5% uptime, but UX must handle 95% gracefully

**Risk 2: Community Data Quality (Spam/Gaming)**
- **Scenario:** Bad actors submit false TSA wait times to game system
- **Mitigation:** Weight community data by user reputation (V1: basic spam detection, V2: ML-based trust scoring), cross-validate against MyTSA API, outlier detection (flag reports >3σ from median)
- **Fallback:** Reduce community weight from 70% to 30% if spam detected, rely more on official APIs

**Risk 3: Confidence Algorithm Rejection**
- **Scenario:** Users don't trust single score, want granular data
- **Mitigation:** Expand/collapse UI pattern (confidence score primary, tap to see detailed breakdown), A/B test algorithm weights based on user feedback
- **Validation:** If <40% trust confidence score within 3 uses, pivot to multi-score dashboard

**Risk 4: Cold Start Problem (No Community Data)**
- **Scenario:** Launch in small airports with <100 users, insufficient community reports
- **Mitigation:** Focus initial launch on top 20 US airports (covers 65% of air travel), use MyTSA historical data as baseline, explicitly communicate "Limited community data for this airport" with transparency
- **Threshold:** Don't launch airport-specific features until ≥50 active users per month in that market

**Risk 5: PWA Browser Incompatibility**
- **Scenario:** Older iOS versions or browser restrictions prevent PWA installation
- **Mitigation:** Responsive web design as baseline (works without install), detect browser capabilities and recommend Chrome/Safari, V2 native app fallback for users who can't install PWA
- **Monitoring:** Track browser analytics, prioritize fixes for browsers representing >5% of traffic

## Web App Specific Requirements

### Project-Type Overview

Door-to-Gate Pulse is a **Progressive Web App (PWA)** built with Next.js 14+ and deployed on Vercel. The architecture prioritizes mobile-first design, installability without app store friction, real-time data delivery, and offline resilience for cached travel data. The web app targets occasional travelers accessing the product primarily on mobile devices during pre-trip anxiety periods (24-48 hours before departure) and on-the-go during travel day.

**Technology Stack:**
- **Framework:** Next.js 14+ (App Router for optimal performance and SEO)
- **Hosting:** Vercel (serverless deployment, edge caching, automatic scaling)
- **PWA:** Workbox for service worker management, installable with manifest.json
- **State Management:** React Context + SWR for real-time data fetching and cache management
- **Styling:** Tailwind CSS (rapid development, mobile-first utilities, dark mode support)
- **Type Safety:** TypeScript for runtime confidence and maintainability

### Browser & Platform Support Matrix

**Primary Platforms (95% of users):**
- **iOS Safari:** 16.4+ (improved PWA support with push notifications, home screen installation)
- **Android Chrome:** Current version and previous 2 major versions (85+ market share on Android)
- **Mobile viewport:** 375px-430px (iPhone SE to iPhone 15 Pro Max)

**Secondary Platforms (5% of users):**
- **Desktop Chrome/Safari/Edge:** Current version (for pre-trip planning at home/office)
- **Desktop viewport:** 1280px-1920px (reference but not primary optimization target)

**Explicit Non-Support:**
- Internet Explorer (no longer supported by Microsoft)
- iOS Safari <16.4 (graceful degradation: web app works but PWA installation unavailable)
- Android browsers other than Chrome (graceful degradation: web app functional, PWA features limited)

**Feature Detection Strategy:**
- Detect PWA capabilities on load and display installation prompt when supported
- Detect notification permissions and request strategically (after first confidence score view, not on landing)
- Fallback to web-only experience if PWA unavailable (no blocking, full functionality accessible)

### Responsive Design Requirements

**Mobile-First Architecture:**
- Primary design target: iPhone viewport 390px × 844px (iPhone 14/15 standard)
- Single-column layout for all mobile breakpoints (<768px)
- Touch-optimized UI: 44px minimum touch targets (WCAG 2.1 AA)
- Bottom-navigation for critical actions (confidence refresh, community report, settings)

**Breakpoint Strategy:**
- **Mobile (default):** 0-767px — Single column, bottom nav, confidence score dominant (70% of viewport)
- **Tablet:** 768px-1023px — Two-column layout, confidence score left, data cards right
- **Desktop:** 1024px+ — Three-column dashboard, confidence score center, data cards flanking

**Dark Mode Support (Critical for Anxiety Reduction):**
- Default to system preference (prefers-color-scheme media query)
- Manual override toggle in settings (some users associate dark mode with "calming")
- High contrast in dark mode for confidence score (80%+ white on dark background)
- Avoid pure black (#000) — use #0a0a0a for reduced eye strain

**Orientation Handling:**
- Portrait primary (95% of mobile usage during travel)
- Landscape supported but not optimized (same layout, horizontal scroll if needed)

### Performance Targets

**Initial Load Performance (First-Time Visitor):**
- **Time to First Byte (TTFB):** <500ms (Vercel edge caching)
- **Largest Contentful Paint (LCP):** <2.0s on 4G connection (Core Web Vital threshold)
- **First Input Delay (FID):** <100ms (interactivity for tap on confidence score)
- **Cumulative Layout Shift (CLS):** <0.1 (skeleton loaders prevent layout shifts)

**Returning User Performance (Service Worker Active):**
- **App Shell Load:** <500ms (cached HTML/CSS/JS)
- **Confidence Score Display:** <1.0s (API fetch or cached data if offline)
- **Full Dashboard Paint:** <1.5s (progressive loading: score first, then data cards)

**Runtime Performance:**
- **Confidence Recalculation:** <500ms (client-side algorithm with Web Workers for heavy computation)
- **Community Report Submission:** <2s round-trip (optimistic UI update, background sync)
- **Real-Time Data Refresh:** 30-second polling interval for active users, WebSocket upgrade in V2
- **Notification Delivery:** <5s from trigger event (push notification via service worker)

**Bundle Size Targets:**
- **Initial JavaScript:** <150KB gzipped (Next.js code splitting, tree shaking)
- **Total Page Weight:** <500KB on initial load (images lazy-loaded, third-party scripts deferred)
- **Service Worker:** <50KB (critical caching logic only)

**Performance Monitoring:**
- Vercel Analytics for Core Web Vitals tracking
- Real User Monitoring (RUM) for 95th percentile performance (target anxious users on slower connections)
- Lighthouse CI in deployment pipeline (block deployment if score <90 for Performance)

### SEO & Discovery Strategy

**SEO Priority: Medium-High**
Organic search is secondary to word-of-mouth but critical for long-tail discovery ("how to know if I'll make my flight", "airport confidence score", "travel anxiety app").

**Technical SEO Requirements:**
- **Server-Side Rendering (SSR):** Next.js SSR for landing page, blog content, airport-specific pages
- **Metadata:** Dynamic OpenGraph tags for social sharing (Sarah shares link with David)
- **Structured Data:** Schema.org SoftwareApplication, AggregateRating (future: community reviews)
- **Sitemap:** Auto-generated XML sitemap for airport pages, blog posts, core pages
- **Robots.txt:** Allow all crawlers, disallow /api/ endpoints and user-specific pages

**Content Strategy for SEO:**
- **Landing Page:** Target "travel anxiety app", "flight confidence score", "door to gate time calculator"
- **Airport Pages:** "/airports/[iata-code]" for top 20 US airports (SEO + direct airport bookmarking)
- **Blog/Resources:** "How to reduce travel anxiety", "When to leave for the airport", "TSA wait time tips"
- **FAQ Page:** Target long-tail "what if" questions ("what if I miss my flight", "how early should I arrive")

**Social Sharing Optimization:**
- **OpenGraph Tags:** Dynamic titles, descriptions, images for each page
- **Twitter Cards:** Summary card with confidence score preview (if user shares active trip)
- **Share Functionality:** "Share my confidence score" button for users to text/message travel companions
- **Preview Image:** Generate dynamic OG image with confidence score visualization (Vercel OG Image)

**Analytics & Attribution:**
- Google Analytics 4 for traffic sources and conversion tracking
- UTM parameter support for campaign tracking
- Referral tracking (where did users find the app? Reddit, travel blogs, family share?)

### Accessibility Requirements (WCAG 2.1 AA)

**Color Contrast & Visual Design:**
- **Confidence Score Colors:** Ensure 4.5:1 contrast ratio for all color thresholds
  - Green (80%+): #10b981 on white, #a7f3d0 on dark
  - Yellow (60-79%): #f59e0b on white, #fcd34d on dark
  - Red (<60%): #ef4444 on white, #fca5a5 on dark
- **Text Contrast:** 4.5:1 for body text, 3:1 for large text (18pt+)
- **Focus Indicators:** 2px solid border on all interactive elements (not rely on color alone)

**Keyboard Navigation:**
- All features accessible via keyboard (Tab, Enter, Escape)
- Logical tab order: Confidence score → Data cards → Community reports → Bottom nav
- Skip links for screen readers ("Skip to confidence score", "Skip to main content")

**Screen Reader Support:**
- ARIA labels for all icons and visual-only elements
- Live regions for confidence score updates ("Confidence score updated to 87%")
- Semantic HTML (nav, main, article, section) for document structure
- Alt text for all images (mockups, airport maps, icons)

**Anxiety-Focused Accessibility Considerations:**
- **Reduced Motion:** Respect prefers-reduced-motion for users with anxiety/vestibular disorders
- **Font Sizes:** Minimum 16px base font, user can zoom to 200% without breaking layout
- **Simple Language:** Avoid jargon ("gate arrival confidence" not "ETA probability distribution")
- **Error Prevention:** Confirm before critical actions ("Delete trip?", "Cancel notifications?")
- **Timeout Extensions:** No automatic logouts during active trip (anxiety-inducing)

**Testing Requirements:**
- Automated testing with axe-core in CI/CD pipeline
- Manual testing with screen readers (VoiceOver on iOS, TalkBack on Android)
- Lighthouse Accessibility score >95 required to merge PRs

### PWA-Specific Features

**Installation Experience:**
- **Manifest.json:** App name, icons (192px, 512px), theme color, background color, display mode (standalone)
- **Installation Prompt:** Custom prompt after user views confidence score (not immediate on landing)
- **Add to Home Screen:** iOS Safari prompt, Android Chrome automatic prompt
- **App Icons:** Designed for iOS home screen (rounded square) and Android (adaptive icon)

**Service Worker Capabilities:**
- **Offline Support:** Cache confidence score, flight data, community reports for last-viewed trip
- **Background Sync:** Queue community reports if offline, submit when connection restored
- **Push Notifications:** Critical alerts ("Leave now", "Traffic delay detected", "Gate change")
- **Cache Strategy:**
  - App shell: Cache-first (immediate load)
  - API data: Network-first with cache fallback (fresh data prioritized)
  - Static assets: Cache-first with stale-while-revalidate

**Notification Strategy:**
- **Permission Request:** After first confidence score view (not on landing — avoid rejection)
- **Notification Types:**
  - Time-sensitive: "Leave in 15 minutes for 85% confidence" (red → yellow threshold crossing)
  - Updates: "Confidence increased to 92%" (yellow → green threshold crossing)
  - Alerts: "Traffic delay detected on your route" (real-time API event)
  - Community: "New TSA wait report at DEN Terminal A" (if user opted into community alerts)
- **Quiet Hours:** No notifications 10pm-6am local time (unless user explicitly enables)
- **Notification Actions:** "View Details", "Snooze 10 min", "Dismiss"

**App-Like Experience:**
- **Splash Screen:** Custom splash screen matching brand colors during PWA launch
- **Status Bar:** Translucent status bar on iOS (blend with app header)
- **No Browser Chrome:** Full-screen experience when installed (no Safari UI, no back button)
- **Pull-to-Refresh:** Native pull-to-refresh gesture for confidence score update

### Real-Time Data Architecture

**MVP: Polling Strategy**
- **Active Polling:** 30-second interval when user has app open and active trip
- **Background Polling:** 5-minute interval when PWA installed but backgrounded (if permission granted)
- **Smart Polling:** Increase frequency to 10s when confidence <70% (critical window)
- **Efficient Polling:** HEAD request first to check ETag, only fetch full data if changed

**V2: WebSocket Upgrade**
- **Real-Time Push:** WebSocket connection for live confidence updates, community reports
- **Fallback:** Graceful degradation to polling if WebSocket unavailable
- **Battery Optimization:** Close WebSocket after 10 minutes of inactivity

**API Integration Requirements:**
- **Rate Limiting:** 60 requests/minute per user for confidence API (prevent abuse)
- **Caching Headers:** ETag and Cache-Control for conditional requests
- **Error Handling:** Graceful degradation if API unavailable (show cached data + "Last updated 5 min ago")
- **Retry Logic:** Exponential backoff for failed API requests (prevent thundering herd)

### Implementation Considerations

**Development Workflow:**
- **Local Development:** Next.js dev server with HTTPS (PWA requires secure context)
- **Preview Deployments:** Vercel preview URLs for every PR (test PWA installation on real devices)
- **Production Deployment:** Vercel production with automatic rollback on failure

**Testing Strategy:**
- **Unit Tests:** Jest + React Testing Library for components and confidence algorithm
- **Integration Tests:** Playwright for critical user flows (view confidence, submit report, install PWA)
- **E2E Tests:** Lighthouse CI for performance regression detection
- **Device Testing:** BrowserStack for real iOS/Android device testing

**Security Considerations:**
- **HTTPS Only:** Enforce HTTPS (PWA requirement + security best practice)
- **Content Security Policy:** Strict CSP to prevent XSS attacks
- **API Authentication:** JWT tokens for authenticated requests (community reports, user preferences)
- **Rate Limiting:** Cloudflare or Vercel edge functions for DDoS protection

**Monitoring & Observability:**
- **Error Tracking:** Sentry for client-side error monitoring
- **Performance Monitoring:** Vercel Analytics for Core Web Vitals
- **API Monitoring:** Datadog or similar for API health and latency
- **User Analytics:** PostHog or similar for product analytics (funnel analysis, retention cohorts)

## Project Scoping & Phased Development

### MVP Strategy & Philosophy

**MVP Approach:** **Experience MVP** — Must deliver anxiety reduction through confidence scoring within first use (trust-building within 3 uses per success criteria). The product fails if it doesn't reduce anxiety better than manually checking 4-6 fragmented apps.

**MVP Success Definition:** Sarah uses it for her next trip and arrives at airport with reduced stress and appropriate timing (not 3 hours early). NPS 40+ by Month 3.

**MVP Resource Requirements:**
- **Team:** 1 full-stack Next.js developer, 1 designer (PWA + anxiety-focused UX), 1 PM (API research + community strategy)
- **Timeline:** 10-14 weeks to launch (top 20 airports only, +2 weeks for Google Auth and database setup)
- **Budget:** API costs ($500/month for FlightAware, Google Maps, OpenWeatherMap), Vercel hosting + PostgreSQL ($50/month for Vercel Pro with database), monitoring tools ($100/month), Google OAuth setup (free)

### MVP Feature Set (Phase 1: Months 1-3)

**Core User Journeys Supported:**
- **Sarah's Anxiety-to-Confidence Journey (Primary):** Full end-to-end from home to gate arrival with confidence scoring
- **David's Indirect Benefit (Secondary):** View-only confidence sharing via URL (no authentication required)
- **Mike's Basic Contribution (Enhanced):** Community reporting with attribution for authenticated users

**Must-Have Capabilities:**

1. **Confidence Dashboard (Core Value)**
   - Single 0-100% confidence score with color-coded thresholds (green 80%+, yellow 60-79%, red <60%)
   - Real-time recalculation (<500ms) with 30-second polling
   - Breakdown view: Drive time, TSA wait, flight status, weather impact (tap to expand)
   - "Leave by" recommendation with countdown timer

2. **Data Aggregation Engine (4 Critical APIs)**
   - **Google Maps/Mapbox:** Real-time traffic and drive time from user location to airport
   - **FlightAware/AviationStack:** Flight status, incoming aircraft tracking, gate information
   - **OpenWeatherMap:** Airport weather conditions and delay probability
   - **MyTSA API:** Baseline TSA wait times (supplemented by community data)
   - Graceful degradation if API fails (cached data with "Last updated X min ago" transparency)

3. **Simplified Community Reporting (Waze-Lite)**
   - **TSA wait time reports only** (not traffic, not gate changes — reduce complexity)
   - Single-tap reporting: "Just cleared TSA: 5 min / 15 min / 30+ min"
   - Display community reports on dashboard with timestamps
   - **Anonymous and authenticated reporting:** Anonymous users can report (IP-based rate limiting), authenticated users get attribution ("Ben reported 5 min ago")
   - Basic spam detection: flag reports >3σ from median, weight authenticated reports higher than anonymous
   - **Report history:** Authenticated users can see their contribution history (foundation for V2 reputation)

4. **PWA Essentials (Installation + Notifications)**
   - Installable from web (iOS Safari 16.4+, Android Chrome)
   - Manifest.json with app icons, theme colors, standalone display mode
   - Service worker for offline confidence score caching (saved trips for authenticated users, last-viewed trip for anonymous)
   - **Push notifications (critical only):** "Leave in 15 minutes" when confidence drops below 70%
   - Opt-in notification permission (after first confidence score view, not on landing)

5. **Google Authentication (Optional but Encouraged)**
   - **Sign in with Google** OAuth 2.0 integration (NextAuth.js)
   - **Anonymous mode fallback:** Users can use app without signing in (localStorage only, single active trip)
   - **Authenticated benefits:** Multi-device sync, saved trips (up to 5 active trips), user preferences (preferred buffer times, notification settings), community attribution
   - **Privacy-first:** Only request email and profile (no access to Google Drive, Calendar, etc.)
   - **No password management:** Eliminate authentication friction while enabling persistence

6. **Trip Setup Flow (Minimal Friction)**
   - Enter flight number OR select airport + departure time
   - Enter departure location (use browser geolocation if permitted, or manual address)
   - Set preferred arrival buffer (default 45 min before departure, adjustable 15-90 min)
   - **Optional trip saving:** If authenticated, option to save trip for multi-device access
   - **Quick re-entry:** Autofill previous airports/locations for returning users (authenticated only)

7. **Responsive Web Interface (Mobile-First)**
   - Mobile-optimized (375px-430px primary viewport)
   - Dark mode support (anxiety-reducing UX)
   - WCAG 2.1 AA compliance (color contrast, keyboard navigation, screen reader support)
   - <2s initial load on 4G, <1s returning users with service worker

**Explicitly Excluded from MVP:**

- ❌ Custom username/password authentication (Google Auth only, reduces security burden)
- ❌ More than 5 saved trips for authenticated users (limit storage for MVP, expand in V2)
- ❌ Social authentication beyond Google (Apple Sign In, Facebook — add in V2 if demand exists)
- ❌ Historical accuracy tracking (no post-trip "How did we do?" survey until V2)
- ❌ Community reports beyond TSA waits (traffic, gate changes, bathroom cleanliness — V2+)
- ❌ Turbulence forecasts (turbli.com integration — V2, not critical for anxiety reduction)
- ❌ WebSocket real-time updates (polling sufficient for MVP, WebSocket in V2)
- ❌ Airport-specific features (terminal maps, parking recommendations — V3)
- ❌ AI-driven predictions (personalized anxiety triggers, pattern learning — V3)
- ❌ Social features (follow Mike, leaderboards, community reputation system — V2+)
- ❌ Airports beyond top 20 US (focus launch, expand in V2 based on demand)

### Post-MVP Features

**Phase 2: Growth (Months 4-12) — Retention & Network Effect**

*Goal: Build community network effect, improve accuracy with learning, scale to 100K users*

**User Features:**
- **Enhanced Authentication:** Add Apple Sign In, email/password fallback for non-Google users
- **Unlimited Saved Trips:** Remove 5-trip limit, add trip history and archiving
- **Enhanced Community Platform:** Mike's full contribution loop with reputation system based on report history, expanded report types (traffic delays, gate changes), community feed with real-time updates
- **Post-Trip Validation:** "How did we do?" survey to track accuracy (target 90% by Month 12)
- **Notification Intelligence:** Adaptive alert timing based on user behavior patterns
- **Turbulence Integration:** turbli.com API for weather anxiety
- **WebSocket Real-Time:** Replace polling with WebSocket for <5s update latency

**Platform Features:**
- **Operations Dashboard (Jennifer's Journey):** Platform health monitoring, API uptime tracking, confidence algorithm accuracy metrics, community contribution analytics
- **Expanded Airport Coverage:** Top 50 US airports (cover 85% of air travel)
- **API Fallback Strategy:** Secondary API integrations (AviationStack backup for FlightAware)
- **Machine Learning:** Confidence algorithm weight optimization based on historical accuracy data

**Phase 3: Expansion (Months 13-24) — Ecosystem & Moat**

*Goal: Build defensible moat through AI, partnerships, international expansion*

**Advanced Features:**
- **AI-Powered Predictions:** Personalized anxiety triggers, predictive recommendations ("Based on your typical drive time, leave at 2:15pm"), pattern recognition across community data for anomaly detection
- **International Expansion:** Top 20 global airports (LHR, CDG, NRT, SYD), localization for non-US travelers
- **Partnership Integrations:** TripIt integration (import itineraries), airline partnerships (official TSA PreCheck/Clear data)
- **Airport-Specific Enhancements:** Terminal maps, parking recommendations, food/retail recommendations, bathroom availability, charging station locations
- **Premium Features (Revenue V3):** Ad-free experience, priority notifications, trip history analytics, family/group trip coordination
- **Native App Consideration:** If PWA adoption <60%, build native iOS/Android apps for app store distribution

**Out of Scope (Not Roadmapped):**
- Ground transportation booking (Uber/Lyft integration) — partnership complexity
- Hotel/car rental integration — out of core anxiety-reduction focus
- Gamification/points — risks undermining anxiety-reduction focus with competitive stress
- Corporate/business travel features — different user psychology than anxious occasional travelers

### MVP Development Phases

**Phase 1a: Foundation (Weeks 1-4)**
- Next.js PWA skeleton with Tailwind CSS, TypeScript setup
- NextAuth.js integration with Google OAuth provider
- Database setup (PostgreSQL on Vercel or Supabase) for user profiles, saved trips, community reports
- Confidence algorithm implementation (client-side calculation with weights)
- Google Maps API integration (drive time calculation)
- FlightAware API integration (flight status lookup)
- Basic trip setup flow (flight number input, departure location, buffer settings)

**Phase 1b: Data Integration (Weeks 5-9)**
- OpenWeatherMap API integration (weather impact calculation)
- MyTSA API integration (baseline TSA wait times)
- Community reporting with authenticated attribution (database-backed)
- Anonymous fallback mode (localStorage for non-authenticated users)
- Service worker implementation (offline caching, background sync)
- Push notification infrastructure (permission request flow, critical alerts only)

**Phase 1c: Polish & Launch (Weeks 10-14)**
- Multi-device sync for authenticated users (saved trips across devices)
- Responsive design refinement (mobile-first optimization)
- Accessibility audit (WCAG 2.1 AA compliance, Lighthouse >95)
- Performance optimization (<2s load time, <500ms confidence recalc)
- Error handling and graceful degradation (API failures, offline mode)
- Beta testing with 50 users (Sarah persona focus groups)
- Launch to top 20 US airports

### Risk Mitigation Strategy

**Technical Risks:**

**Risk:** API reliability failures during peak travel (Thanksgiving, Christmas)
- **Mitigation:** Implement circuit breakers with exponential backoff, cache API responses aggressively, graceful degradation UI ("Flight data temporarily unavailable")
- **Contingency:** Secondary API integrations ready in V2 (AviationStack backup for FlightAware)

**Risk:** Confidence algorithm rejection (users don't trust single score)
- **Mitigation:** Expand/collapse UI pattern (score prominent, tap for detailed breakdown), A/B test algorithm weights with early users
- **Validation:** Track trust metrics in post-trip survey ("Did you trust the confidence score?")
- **Pivot Threshold:** If <40% trust within 3 uses, pivot to multi-score dashboard

**Risk:** Google Auth dependency (users don't want to sign in with Google, privacy concerns)
- **Mitigation:** Anonymous mode as fully-functional fallback (no forced sign-in), clear privacy policy (only email/profile requested)
- **Validation:** Track anonymous vs authenticated usage ratio, target 60% authenticated by Month 3
- **Contingency:** Add Apple Sign In in V2 if iOS users reject Google Auth

**Risk:** Database costs at scale (PostgreSQL costs increase with user growth)
- **Mitigation:** Start with Vercel Postgres (generous free tier), implement aggressive data retention (delete trips >30 days old for inactive users)
- **Contingency:** Migrate to self-hosted PostgreSQL on Railway/Fly.io if costs exceed $200/month

**Market Risks:**

**Risk:** Cold start problem (no community data in early markets)
- **Mitigation:** Focus launch on top 20 airports (65% of US air travel), use MyTSA historical data as baseline, explicitly communicate "Limited community data" with transparency
- **Validation:** Don't launch airport-specific features until ≥50 active users/month in that market
- **Growth Strategy:** Incentivize early community reporting with attribution (authenticated users see "You've contributed 12 reports")

**Risk:** User acquisition failure (anxious travelers don't discover product)
- **Mitigation:** SEO investment (target "travel anxiety app", "flight confidence score"), content marketing (blog posts on anxiety reduction), Reddit/travel community outreach
- **Validation:** Track referral sources (organic search, social, word-of-mouth), pivot marketing channels if organic <30% by Month 6
- **Contingency:** Partnership with travel bloggers/influencers focusing on family travel

**Risk:** Competitive response (TripIt, FlightAware add confidence scoring)
- **Mitigation:** Community network effect as moat (competitors can't replicate data quality quickly), anxiety-focused UX as differentiation (not just data aggregation)
- **Validation:** Monitor competitor feature releases, accelerate V2 community features if competitive threat detected

**Resource Risks:**

**Risk:** MVP takes longer than 14 weeks (Google Auth + database adds complexity)
- **Mitigation:** Use NextAuth.js boilerplate for rapid Google Auth setup, use Vercel Postgres for zero-config database
- **Contingency:** Launch without saved trips (localStorage only), add Google Auth in V1.1 update 2 weeks later

**Risk:** API costs exceed budget (FlightAware $200/month → $2000/month with scale)
- **Mitigation:** Implement aggressive caching (cache flight status for 5 min, not real-time minute-by-minute), rate limit per-user API requests (60/min)
- **Contingency:** Introduce freemium model in V2 (free users get 10-minute cached data, premium users get real-time)

**Risk:** Single developer bottleneck (full-stack developer quits mid-MVP)
- **Mitigation:** Comprehensive documentation from day 1, code reviews for knowledge sharing, TypeScript for maintainability
- **Contingency:** Simplify architecture to make handoff easier (monolithic Next.js app, not microservices)

## Functional Requirements

### Trip Management

- **FR1:** Users can create a trip by entering a flight number with automatic airport/time lookup
- **FR2:** Users can create a trip by manually selecting airport and departure time
- **FR3:** Users can set departure location via browser geolocation
- **FR4:** Users can set departure location via manual address entry
- **FR5:** Users can configure preferred arrival buffer time (15-90 minutes before departure)
- **FR6:** Authenticated users can save up to 5 active trips for multi-device access
- **FR7:** Authenticated users can view their saved trips across devices
- **FR8:** Authenticated users can delete saved trips
- **FR9:** Authenticated users can edit trip details (departure location, buffer time)
- **FR10:** Anonymous users can maintain one active trip in browser storage

### Confidence Scoring Engine

- **FR11:** System calculates real-time confidence score (0-100%) combining drive time, TSA wait, weather impact, and flight status
- **FR12:** System applies weighted algorithm (TSA 70%, traffic 35%, weather 120%, flight status variable)
- **FR13:** System recalculates confidence score within 500ms of data changes
- **FR14:** System refreshes confidence data every 30 seconds for active trips
- **FR15:** System displays color-coded confidence thresholds (green 80%+, yellow 60-79%, red <60%)
- **FR16:** Users can view confidence score breakdown showing individual data source contributions
- **FR17:** System calculates "leave by" recommendation time based on confidence score and user buffer
- **FR18:** System displays countdown timer to recommended departure time
- **FR19:** System increases polling frequency to 10 seconds when confidence drops below 70%

### Data Aggregation & External APIs

- **FR20:** System retrieves real-time traffic data and drive time from user location to airport
- **FR21:** System retrieves flight status, incoming aircraft tracking, and gate information
- **FR22:** System retrieves airport weather conditions and calculates delay probability
- **FR23:** System retrieves baseline TSA wait times from MyTSA API
- **FR24:** System gracefully degrades when API is unavailable, displaying cached data with last-update timestamp
- **FR25:** System implements exponential backoff retry logic for failed API requests
- **FR26:** System caches API responses to minimize redundant requests

### Community Reporting

- **FR27:** Users can submit TSA wait time reports with three options (5 min, 15 min, 30+ min)
- **FR28:** Authenticated users receive attribution for community reports (name + timestamp)
- **FR29:** Anonymous users can submit community reports with IP-based rate limiting
- **FR30:** System displays community reports on dashboard with timestamps and attribution
- **FR31:** Authenticated users can view their community report history
- **FR32:** System flags community reports that deviate >3σ from median as potential spam
- **FR33:** System weights authenticated community reports higher than anonymous reports
- **FR34:** System integrates community TSA reports into confidence score calculation

### User Authentication

- **FR35:** Users can sign in with Google OAuth 2.0
- **FR36:** Users can use the application without authentication in anonymous mode
- **FR37:** System requests only email and profile information from Google (no calendar/drive access)
- **FR38:** Authenticated users can sign out
- **FR39:** System maintains user session across browser sessions for authenticated users
- **FR40:** System syncs user preferences across devices for authenticated users

### Push Notifications

- **FR41:** System requests push notification permission after user views first confidence score
- **FR42:** Users can grant or deny push notification permission
- **FR43:** System sends critical notification when confidence drops below 70% with "leave in X minutes" guidance
- **FR44:** System sends update notification when confidence crosses threshold boundaries (red→yellow, yellow→green)
- **FR45:** System sends alert notification when traffic delay is detected on user's route
- **FR46:** System respects quiet hours (10pm-6am local time) unless user explicitly opts in
- **FR47:** Users can configure notification preferences (enable/disable by type)
- **FR48:** Notifications include actionable buttons ("View Details", "Snooze 10 min", "Dismiss")

### Progressive Web App Features

- **FR49:** System provides installable PWA manifest with app icons, theme colors, and standalone display mode
- **FR50:** System displays custom installation prompt after user views confidence score
- **FR51:** System implements service worker for offline caching of active trip data
- **FR52:** System caches app shell (HTML/CSS/JS) for <500ms load time on returning visits
- **FR53:** System queues community reports for background sync when offline
- **FR54:** System submits queued community reports when connection is restored
- **FR55:** System displays offline status indicator when no network connection is detected
- **FR56:** System provides pull-to-refresh gesture for manual confidence score updates

### Content Sharing & Collaboration

- **FR57:** Users can generate shareable link for their trip confidence score
- **FR58:** Non-authenticated users can view shared trip confidence scores via link
- **FR59:** Shared trip views display read-only confidence score without requiring authentication
- **FR60:** Shared trip views update in real-time with current confidence data

### User Interface & Experience

- **FR61:** System displays responsive design optimized for mobile viewports (375px-430px)
- **FR62:** System provides dark mode based on system preference or manual toggle
- **FR63:** System maintains WCAG 2.1 AA color contrast ratios for all UI elements
- **FR64:** System supports keyboard navigation for all interactive elements
- **FR65:** System provides ARIA labels and semantic HTML for screen reader accessibility
- **FR66:** System respects prefers-reduced-motion setting for users with vestibular disorders
- **FR67:** System allows text zoom to 200% without breaking layout
- **FR68:** System provides skip links for screen readers to jump to main content
- **FR69:** System displays focus indicators for keyboard navigation
- **FR70:** System provides touch-optimized controls with 44px minimum touch targets

### Airport & Flight Coverage

- **FR71:** System supports confidence scoring for top 20 US airports (MVP)
- **FR72:** System displays airport coverage status ("Limited data for this airport" for unsupported airports)
- **FR73:** System parses flight numbers to identify airline, flight, date, and routing
- **FR74:** System validates flight numbers and provides error feedback for invalid entries

### Performance & Reliability

- **FR75:** System loads initial page in <2 seconds on 4G connection for first-time visitors
- **FR76:** System loads app shell in <500ms for returning users with service worker
- **FR77:** System displays skeleton loaders to prevent layout shift during data loading
- **FR78:** System implements client-side confidence calculation with <500ms computation time

### Data Privacy & Security

- **FR79:** System stores user preferences and saved trips in database for authenticated users
- **FR80:** System stores active trip in browser localStorage for anonymous users
- **FR81:** System deletes trips older than 30 days for inactive users
- **FR82:** System implements JWT token authentication for API requests
- **FR83:** System rate limits API requests to 60 per minute per user

## Non-Functional Requirements

### Performance

**Response Time Requirements:**
- **NFR1:** Initial page load completes in <2.0 seconds on 4G connection (LCP metric)
- **NFR2:** Returning user app shell loads in <500ms with service worker active
- **NFR3:** Confidence score recalculation completes in <500ms from data change trigger
- **NFR4:** User interactions respond within <100ms (First Input Delay metric)
- **NFR5:** API data refresh polling cycle completes within 30-second interval for active trips
- **NFR6:** Critical polling frequency increases to 10-second interval when confidence <70%

**Bundle & Asset Performance:**
- **NFR7:** Initial JavaScript bundle size remains <150KB gzipped
- **NFR8:** Total page weight stays <500KB on initial load
- **NFR9:** Service worker file size remains <50KB
- **NFR10:** Cumulative Layout Shift (CLS) metric stays <0.1

**Real-Time Data Performance:**
- **NFR11:** Community report submission completes round-trip in <2 seconds
- **NFR12:** Push notification delivery occurs within <5 seconds of trigger event
- **NFR13:** Confidence dashboard displays updated score within <1.0 second of data fetch

**Performance Monitoring:**
- **NFR14:** Core Web Vitals tracked via Vercel Analytics for 95th percentile performance
- **NFR15:** Lighthouse Performance score maintains >90 in CI/CD pipeline (deployment blocker)

### Security

**Authentication & Authorization:**
- **NFR16:** All user authentication implements OAuth 2.0 via NextAuth.js
- **NFR17:** System enforces HTTPS-only connections (no HTTP fallback)
- **NFR18:** JWT tokens expire after 7 days requiring re-authentication
- **NFR19:** API requests include valid JWT token or fail with 401 Unauthorized
- **NFR20:** Google OAuth requests minimum scope (email + profile only, no calendar/drive)

**Data Protection:**
- **NFR21:** User passwords never stored (OAuth only, no custom password authentication)
- **NFR22:** Database connections use encrypted connections (SSL/TLS)
- **NFR23:** API keys stored as environment variables, never committed to version control
- **NFR24:** User data automatically deleted after 30 days of inactivity

**Application Security:**
- **NFR25:** Content Security Policy (CSP) headers prevent XSS attacks
- **NFR26:** Rate limiting enforces max 60 API requests per minute per user
- **NFR27:** Anonymous community reports limited by IP-based rate limiting (max 10 reports/hour)
- **NFR28:** Client-side input validation prevents injection attacks

**Privacy Compliance:**
- **NFR29:** Anonymous mode requires no personal data collection
- **NFR30:** Authenticated users can delete all personal data on request
- **NFR31:** No third-party tracking scripts (Google Analytics only, no Meta Pixel, etc.)

### Scalability

**User Growth Targets:**
- **NFR32:** System supports 5,000 active users by Month 3 without performance degradation
- **NFR33:** System scales to 100,000 active users by Month 12 with <10% performance impact
- **NFR34:** Database handles 1 million saved trips with <500ms query response times

**Traffic Handling:**
- **NFR35:** System handles peak travel periods (Thanksgiving, Christmas) with 10x normal traffic
- **NFR36:** Serverless functions auto-scale to handle concurrent user load spikes
- **NFR37:** CDN caching handles static asset delivery for global user base

**API Integration Scalability:**
- **NFR38:** Aggressive caching reduces external API calls by >70% vs naive real-time requests
- **NFR39:** Circuit breakers prevent cascading failures when external APIs slow down
- **NFR40:** Connection pooling limits database connections to prevent resource exhaustion

**Cost Scalability:**
- **NFR41:** API costs remain <$1,000/month at 10,000 active users
- **NFR42:** Database costs remain <$200/month at 100,000 users with retention policy
- **NFR43:** Vercel hosting costs remain <$100/month with edge caching optimization

### Accessibility

**WCAG 2.1 AA Compliance:**
- **NFR44:** All UI elements maintain 4.5:1 color contrast ratio for body text
- **NFR45:** Large text (18pt+) maintains 3:1 color contrast ratio
- **NFR46:** All interactive elements include 2px solid border focus indicators
- **NFR47:** Touch targets meet 44px minimum size for mobile accessibility

**Keyboard Navigation:**
- **NFR48:** All features fully accessible via keyboard (Tab, Enter, Escape)
- **NFR49:** Logical tab order follows visual hierarchy (confidence score → cards → nav)
- **NFR50:** Skip links enable screen reader users to jump to main content

**Screen Reader Support:**
- **NFR51:** All icons include ARIA labels for screen reader accessibility
- **NFR52:** ARIA live regions announce confidence score updates
- **NFR53:** Semantic HTML elements (nav, main, article) provide document structure
- **NFR54:** All images include descriptive alt text

**Anxiety-Focused Accessibility:**
- **NFR55:** System respects prefers-reduced-motion for users with vestibular disorders
- **NFR56:** Base font size minimum 16px, zoom up to 200% without layout breaking
- **NFR57:** No automatic timeouts during active trip (anxiety-inducing)
- **NFR58:** Error messages provide clear recovery actions (no technical jargon)

**Testing & Compliance:**
- **NFR59:** Automated axe-core testing in CI/CD pipeline catches accessibility regressions
- **NFR60:** Lighthouse Accessibility score >95 required to merge PRs
- **NFR61:** Manual screen reader testing (VoiceOver iOS, TalkBack Android) before release

### Integration Reliability

**External API Dependencies:**
- **NFR62:** System implements exponential backoff for failed API requests (1s, 2s, 4s, 8s intervals)
- **NFR63:** Graceful degradation displays cached data when API unavailable
- **NFR64:** API timeout limits prevent request hanging (5-second max per API call)
- **NFR65:** Health checks monitor API availability every 60 seconds

**API Failure Handling:**
- **NFR66:** Google Maps API failure falls back to cached drive times from previous requests
- **NFR67:** FlightAware API failure displays "Flight data temporarily unavailable" with last update timestamp
- **NFR68:** OpenWeatherMap API failure defaults to "unknown" weather impact (excludes from confidence)
- **NFR69:** MyTSA API failure relies solely on community TSA reports

**Data Consistency:**
- **NFR70:** Community reports submitted offline queue for background sync
- **NFR71:** Saved trips sync across devices within 10 seconds of login
- **NFR72:** Confidence score calculation uses most recent available data from each API (mixed freshness acceptable)

**API Performance:**
- **NFR73:** ETag-based conditional requests reduce bandwidth for unchanged API data
- **NFR74:** API response caching prevents duplicate requests within 5-minute window
- **NFR75:** Parallel API requests complete within 3 seconds aggregate (not sequential)

### Reliability & Availability

**Uptime Targets:**
- **NFR76:** Application uptime maintains 99.5% monthly (max 3.6 hours downtime/month)
- **NFR77:** Database uptime maintains 99.9% monthly via Vercel/Supabase SLA
- **NFR78:** Service worker ensures offline functionality for cached trips

**Error Recovery:**
- **NFR79:** Client-side errors logged to Sentry for monitoring and alerting
- **NFR80:** Critical errors display user-friendly messages with recovery actions
- **NFR81:** Failed community report submissions retry automatically when connection restored
- **NFR82:** Corrupted localStorage data auto-clears and prompts fresh trip creation

**Monitoring & Alerting:**
- **NFR83:** API health monitoring alerts team when uptime <95% over 1-hour period
- **NFR84:** Performance regression alerts trigger when LCP >2.5 seconds for >25% of users
- **NFR85:** Error rate monitoring alerts when client-side error rate >1% of sessions

**Data Integrity:**
- **NFR86:** Database transactions ensure atomic updates (trip save succeeds completely or fails completely)
- **NFR87:** Background sync queues persist across browser sessions
- **NFR88:** Confidence score calculation validates all input data before rendering

### Usability

**Mobile-First Experience:**
- **NFR89:** Primary UI optimization targets 375px-430px mobile viewports
- **NFR90:** Bottom navigation remains accessible with one-handed thumb reach
- **NFR91:** Pull-to-refresh gesture provides intuitive confidence score update

**Dark Mode:**
- **NFR92:** System detects and respects prefers-color-scheme media query
- **NFR93:** Manual dark mode toggle persists across sessions for authenticated users
- **NFR94:** Dark mode uses #0a0a0a background (not pure black #000) for reduced eye strain

**Progressive Web App Experience:**
- **NFR95:** PWA installation requires max 2 taps from prompt to home screen
- **NFR96:** Installed PWA launches in <500ms to splash screen
- **NFR97:** PWA operates offline with degraded functionality (cached data, no API updates)
- **NFR98:** PWA runs in standalone mode without browser chrome
