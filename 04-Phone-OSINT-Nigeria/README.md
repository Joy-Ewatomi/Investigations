# Case Study #4: Phone Number OSINT Investigation - Nigeria Focus

**Investigation Type:** Phone Number Intelligence & Business Verification  
**Date:** November 11, 2025 (Day 22/90)  
**Investigator:** Joy Ewatomi  
**Agency:** ShadowNode Intelligence Agency  
**Location:** Kogi State, Nigeria  
**Duration:** 3 hours  
**Status:** ✅ Complete

---

## 📋 EXECUTIVE SUMMARY

**Objective:** Master phone number OSINT techniques focusing on Nigerian telecommunications, including network identification, business verification, and information discovery through publicly available sources.

**Key Findings:**
- ✅ **100% success rate** - 5/5 phone numbers had WhatsApp Business accounts
- ✅ **Email discovery:** 5/5 numbers revealed associated email addresses
- ✅ **Location intelligence:** 3/5 provided GPS coordinates
- ✅ **Network dominance:** MTN accounts for 80% of investigated business lines
- ✅ **Google Dorking:** 3/3 companies successfully located via site: operator
- 📊 **Information leakage:** Single phone number = name, email, location, business hours, products

**Conclusion:** Phone numbers are powerful intelligence gateways. WhatsApp Business accounts sacrifice privacy for discoverability, revealing comprehensive business profiles. Nigerian businesses primarily use MTN network (80% of sample). All techniques executed with $0 cost using free tools.

---

## 🎯 INVESTIGATION SCOPE

### What Was Investigated:
- Nigerian phone number format and structure
- Mobile network prefix identification (MTN, Glo, Airtel, 9mobile)
- Google Dorking for official business numbers
- WhatsApp Business account intelligence gathering
- Corporate phone number pattern analysis
- Information leakage from phone numbers
- Business verification techniques

### Why This Matters:
Phone number OSINT is critical for:
- **Identity Verification:** Confirm caller legitimacy
- **Scam Detection:** Identify fraudulent numbers vs. official contacts
- **Background Checks:** Profile individuals and businesses
- **Contact Discovery:** Find associated emails, social media, locations
- **Business Intelligence:** Understand corporate communication strategies
- **Privacy Awareness:** Know what your number reveals about you

---

## 🔍 METHODOLOGY

### Investigation Structure: 5 Exercises

**Exercise 1:** Nigerian Phone Number Format Mastery  
**Exercise 2:** Google Dorking for Phone Numbers  
**Exercise 3:** TrueCaller Research (Tool Not Available)  
**Exercise 4:** WhatsApp Phone Number Investigation  
**Exercise 5:** Business Phone Pattern Analysis

---

## 📞 EXERCISE 1: NIGERIAN PHONE NUMBER FORMAT ANALYSIS

### Phone Number Structure

**International Format:**
```
+234 XXX XXX XXXX
```
- Country Code: +234 (Nigeria)
- Network Prefix: XXX (3 digits)
- Subscriber Number: XXX XXXX (7 digits)
- **Total:** 13 digits with country code

**Domestic Format:**
```
0XXX XXX XXXX
```
- Leading Zero: 0
- Network Prefix: XXX (3 digits)
- Subscriber Number: XXX XXXX (7 digits)
- **Total:** 11 digits

### Nigerian Mobile Network Prefixes

#### **MTN Nigeria (Yellow Network)**
Primary prefixes:
- 0803, 0806, 0810, 0813, 0814, 0816
- 0903, 0906

**Market Position:** Largest network in Nigeria  
**Color Branding:** Yellow  
**Ownership:** MTN Group (South African multinational)

#### **Glo Mobile (Green Network)**
Primary prefixes:
- 0805, 0807, 0811, 0815
- 0905

**Market Position:** Second largest  
**Color Branding:** Green  
**Ownership:** Globacom (Nigerian-owned)

#### **Airtel Nigeria (Red Network)**
Primary prefixes:
- 0802, 0808, 0812
- 0901, 0902, 0904, 0907, 0912

**Market Position:** Third largest  
**Color Branding:** Red  
**Ownership:** Bharti Airtel (Indian multinational)

#### **9mobile (formerly Etisalat)**
Primary prefixes:
- 0809, 0817, 0818
- 0908, 0909

**Market Position:** Fourth largest  
**Previous Name:** Etisalat Nigeria  
**Ownership:** Teleology Holdings Limited

### Prefix Pattern Recognition

**Older Prefixes (080X, 081X):**
- Allocated in early 2000s
- More established users
- Often business/corporate lines
- Higher perceived legitimacy

**Newer Prefixes (090X):**
- Allocated after 2010
- More recent subscribers
- Increased mobile penetration
- Can indicate newer businesses

### Network Identification Skill Test

**Practice Result:** 100% accuracy identifying networks from prefixes

**Example Identifications:**
- 0806 → MTN
- 0805 → Glo
- 0802 → Airtel
- 0809 → 9mobile
- 0903 → MTN

**OSINT Value:**
Knowing network helps:
- Verify number authenticity
- Understand number age/establishment
- Detect inconsistencies (e.g., scammer claims old bank but uses new prefix)

---

## 🔎 EXERCISE 2: GOOGLE DORKING FOR PHONE NUMBERS

### Google Dork Methodology

**Basic Formula:**
```
site:[domain] "contact" "+234"
```

**Advanced Formula:**
```
site:[domain] "customer service" OR "contact us" "+234"
```

### Company 1: MTN Nigeria

**Target:** MTN Nigeria (Telecommunications)  
**Website:** mtn.ng

**Google Dork Used:**
```
site:mtn.ng "contact" "+234"
```

**Results:** ✅ Success

**Numbers Found:**
- **+234 903 300 0001** - Zigi Chatbot (Official customer support)
- Multiple customer support lines
- Network-specific contact numbers

**Key Insight:**
Using `site:` operator filters out third-party directories and ensures official information directly from company website.

**Verification:**
- All numbers returned were official MTN contacts
- No spam or scam numbers in results
- Direct from source = highest reliability

### Company 2: Jumia

**Target:** Jumia (E-commerce marketplace)  
**Website:** jumia.com.ng

**Google Dork Used:**
```
site:jumia.com.ng "contact" "+234"
```

**Results:** ✅ Success (Too Many Results)

**Challenge Encountered:**
Marketplace model = hundreds of phone numbers:
- Official Jumia corporate numbers
- Individual seller contact numbers
- Delivery partner numbers
- Vendor support lines
- Third-party logistics contacts

**Problem:**
Cannot distinguish official Jumia numbers from marketplace sellers.

**Solution - Refined Dork:**
```
site:jumia.com.ng "customer service" "+234"
```

**Key Learning:**
For marketplace/multi-vendor platforms:
1. Refine search with specific department keywords
2. Look for "official," "corporate," "headquarters"
3. Check company "About Us" or "Contact Us" pages directly
4. Distinguish company infrastructure from user-generated content

### Company 3: GTBank (Guaranty Trust Bank)

**Target:** Guaranty Trust Bank  
**Website:** gtbank.com

**Method:** Direct website navigation + Google Dorking  
**Page:** gtbank.com/help-centre

**Numbers Found:**

**Corporate Headquarters (Landlines):**
- +234 201 271 4580
- +234 201 271 5227
- Location: Plot 635, Akin Adesola Street, Victoria Island, Lagos

**GTConnect (Customer Service):**
- +234 201 448 0000 (Landline)
- +234 802 900 2900 (Airtel - 0802)
- +234 803 900 3900 (MTN - 0803)
- +234 813 985 6000 (MTN - 0813)

**Toll-Free Number:**
- +234 700 4826 66328
- **Special Feature:** Spells "0700 GTBANK" (mnemonic marketing)

**WhatsApp-Only Line:**
- +234 904 000 2900 (Airtel - 0904)
- Purpose: Dedicated WhatsApp customer service channel

### Google Dorking Success Rate

| Company | Google Dork | Result | Numbers Found |
|---------|-------------|--------|---------------|
| **MTN** | ✅ Success | Official numbers | Multiple |
| **Jumia** | ✅ Success* | (*Requires refinement) | Hundreds |
| **GTBank** | ✅ Success | 7+ official numbers | Complete contact list |

**Overall Success Rate:** 3/3 (100%)

### Key Insights from Google Dorking

**Why It Works:**
- `site:` operator limits results to official domain
- Bypasses third-party directories (outdated/scam numbers)
- Direct from source = highest accuracy
- Faster than manual website navigation

**Best Practices:**
1. Always use `site:` operator for official numbers
2. Combine with "contact" OR "customer service"
3. Include country code in search ("+234" for Nigeria)
4. Refine for marketplace/multi-vendor platforms
5. Cross-verify numbers on multiple company pages

---

## 🔍 EXERCISE 3: TRUECALLER RESEARCH (Tool Not Available)

### Status: Tool Skipped - Theoretical Research Conducted

**TrueCaller Overview:**

**What It Is:**
- Crowdsourced caller ID database
- Global phone number directory
- Spam/scam number identification
- Name and location lookup

**How It Works:**
1. Users install TrueCaller app
2. App uploads user's contact list to database
3. When unknown number calls, app searches database
4. Returns name, location, spam reports if found

**OSINT Applications:**
- ✅ Identify unknown callers
- ✅ Find names associated with numbers
- ✅ Check spam/scam reports
- ✅ Approximate location data
- ✅ Business vs. personal identification

**Privacy Concerns:**
- ⚠️ User contacts uploaded without explicit consent of contacts
- ⚠️ Your number may be in database without your permission
- ⚠️ Names and numbers publicly searchable
- ⚠️ Difficult to remove yourself from database

**Limitations:**
- Only works for numbers already in database
- Requires crowdsourced data (not comprehensive)
- Accuracy depends on user submissions
- May have outdated information

**Alternative Used:** WhatsApp Business investigation (Exercise 4)

**Future Investigation:**
Will test TrueCaller when app access is available for comparison with WhatsApp methodology.

---

## 💬 EXERCISE 4: WHATSAPP PHONE NUMBER INVESTIGATION

### Investigation Methodology

**Process:**
1. Save target phone numbers to device contacts
2. Open WhatsApp and search for contact
3. If WhatsApp account exists, view profile
4. Document all publicly available information
5. Screenshot evidence (business profiles)

**Sample Size:** 5 phone numbers  
**Success Rate:** 5/5 (100%) - All had WhatsApp accounts  
**Account Type:** All were WhatsApp Business accounts

### Detailed Investigation Results

#### **Number 1: +234 806 879 6208**

**Network:** MTN (0806 prefix)

**WhatsApp Account Found:** ✅ Yes

**Business Name:** Dawanau Trade Network Ltd

**Owner Name:** Hassan Ahmad Umar

**Business Category:** Food Wholesaler

**Physical Location:** 
- City: Dawanau, Kano, Nigeria
- GPS Coordinates: Provided on WhatsApp map
- Map: Interactive location pin visible

**Contact Information:**
- Email: maizambrothers@gmail.com
- Website: https://Dawanau.com

**Business Description:**
"We sell best quality agricultural commodities"

**Operating Hours:** Open 24 hours

**Products:** 
- Agricultural commodities
- Product catalog visible on WhatsApp Business

**Account Type:** WhatsApp Business (verified business features)

**Information Leakage Assessment:**
From phone number alone, discovered:
- ✅ Full business name
- ✅ Owner's full name
- ✅ Email address
- ✅ Physical location with GPS
- ✅ Website
- ✅ Business hours
- ✅ Product catalog

#### **Number 2: +234 707 701 8156**

**Network:** Glo (0707 prefix)

**WhatsApp Account Found:** ✅ Yes

**Business Name:** ChiYa Gadgets

**Business Category:** 
- Phone accessories
- Speakers
- Power banks
- Mobile devices

**Product Catalog:** ✅ Visible
- Phone accessories
- Xiaomi Redmi phones
- Bluetooth speakers
- Charging accessories

**Operating Hours:** Open 24 hours

**Account Type:** WhatsApp Business

**Information Available:**
- ✅ Business name
- ✅ Product catalog with images
- ✅ Pricing information (in catalog)
- ✅ Operating hours

**Notable:** 
Glo network (not MTN) - represents 20% of sample showing network diversity.

#### **Number 3: +234 903 300 0001**

**Network:** MTN (0903 prefix)

**WhatsApp Account Found:** ✅ Yes

**Business Name:** Zigi - MTN Chatbot

**Verification Status:** ✅ Blue Checkmark (Official Verified Account)

**Business Category:** MTNN Customer Support

**Physical Location:**
- Address: MTN Plaza, Falomo, Ikoyi, Lagos
- GPS Map: Provided

**Contact Information:**
- Email: whatsappsupporthelpdesk@mtn.com
- Website: www.mtn.ng

**Account Type:** Official Verified Business

**Significance:**
- Official MTN customer support line
- Blue checkmark = Platform-verified authenticity
- Found same number via Google Dorking (Exercise 2)
- Cross-verification confirms legitimacy

**OSINT Value:**
Demonstrates how to identify official company accounts vs. impersonators using verification badges.

#### **Number 4: +234 806 210 6493**

**Network:** MTN (0806 prefix)

**WhatsApp Account Found:** ✅ Yes

**Business Name:** Lifepills

**Business Category:** Other Business (Healthcare/Wellness implied by name)

**Contact Information:**
- Email: lifepillsinternational@gmail.com
- Website: https://lifepillsinternational.org.ng

**Operating Hours:** Open 24 hours

**Account Type:** WhatsApp Business

**Domain Analysis:**
- `.org.ng` domain suggests Nigerian organization
- "International" in name suggests broader reach
- Healthcare/wellness industry (based on "Lifepills" name)

**Information Available:**
- ✅ Business name
- ✅ Email address
- ✅ Website
- ✅ Operating hours
- ✅ Business category

#### **Number 5: +234 806 080 6962**

**Network:** MTN (0806 prefix)

**WhatsApp Account Found:** ✅ Yes

**Account Name:** akinjaiyejuoo

**Business Category:** Professional Educationist / Education

**Physical Location:**
- ISL, Unilag (University of Lagos)
- Education sector affiliation

**Contact Information:**
- Email: akinjaiyejuoo@gmail.com

**About Section:**
"God is working through our current situations to bring us to an expected end. #Dontlosefaith. #keepbelieving. #HeStillCares"

**Account Establishment:** Since May 14, 2017

**Account Age:** 8+ years old (as of Nov 2025)

**Significance:**
- Long-established account (8+ years)
- Account age = credibility indicator
- Educational professional
- Personal/professional blend (faith-based messaging)

**OSINT Insight:**
Account age can indicate:
- Established identity (not newly created for scams)
- Long-term business/professional presence
- Higher likelihood of legitimacy

**Account Type:** WhatsApp Business

### Comprehensive Analysis

#### **Network Distribution**

| Network | Count | Percentage |
|---------|-------|------------|
| **MTN** | 4 | 80% |
| **Glo** | 1 | 20% |
| **Airtel** | 0 | 0% |
| **9mobile** | 0 | 0% |

**Key Finding:** MTN dominates Nigerian business WhatsApp accounts (80% of sample)

**Possible Reasons:**
- MTN is largest network in Nigeria
- Better network coverage
- Business preference for reliable network
- First-mover advantage in mobile data

#### **Information Leakage Matrix**

| Information Type | Found (out of 5) | Percentage |
|------------------|------------------|------------|
| **Business Names** | 5/5 | 100% |
| **Email Addresses** | 5/5 | 100% |
| **Physical Locations** | 3/5 | 60% |
| **Websites** | 4/5 | 80% |
| **Operating Hours** | 4/5 | 80% |
| **Owner Names** | 1/5 | 20% |
| **Product Catalogs** | 2/5 | 40% |
| **GPS Coordinates** | 3/5 | 60% |

**Critical Insight:**
From a phone number alone, investigators can discover:
- ✅ 100% success rate for business names
- ✅ 100% success rate for email addresses
- ✅ 80% success rate for websites
- ✅ 60% success rate for physical locations with GPS

#### **WhatsApp Business Features Observed**

**Profile Components:**
- ✅ Profile photos (business logos/branding)
- ✅ About/description sections
- ✅ Location pins with interactive maps
- ✅ Business hours (24/7 or specific times)
- ✅ Product catalogs with images and prices
- ✅ Contact buttons (call, message, share)
- ✅ Website links (clickable URLs)
- ✅ Email addresses
- ✅ Category classification (industry type)
- ✅ Verification badges (blue checkmarks for official accounts)

**Privacy vs. Discoverability Trade-off:**

**Businesses Choose:**
- ⚠️ Maximum information sharing
- ⚠️ Public profiles for marketing
- ⚠️ Discoverability over privacy

**Why:**
- Marketing: Want customers to find them
- Credibility: Show legitimacy through transparency
- Accessibility: Multiple contact methods
- Competition: Match or exceed competitors' information

**Privacy Implications:**

**For Business Owners:**
- ✅ Intentional public information sharing
- ✅ Trade privacy for customer acquisition
- ⚠️ May not realize full extent of data exposure

**For Individuals:**
- ⚠️ Personal numbers can be linked to businesses
- ⚠️ Owner names may be exposed
- ⚠️ Location data publicly available

**For OSINT Investigators:**
- ✅ WhatsApp Business = Rich intelligence source
- ✅ Legal and ethical (publicly shared information)
- ✅ No technical hacking required
- ✅ Simple contact save + WhatsApp check = Full profile

---

## 🏢 EXERCISE 5: BUSINESS PHONE PATTERN ANALYSIS

### Case Study: GTBank (Guaranty Trust Bank)

**Source:** Official website (gtbank.com/help-centre)

### Phone Number Categories Identified

#### **1. Corporate Landlines**

**Format:** +234 201 XXX XXXX

**Pattern Recognition:**
- "201" = Lagos area code
- Landlines indicate:
  - Corporate headquarters
  - Established physical presence
  - Higher legitimacy perception
  - Professional business operations

**Examples:**
- +234 201 271 4580
- +234 201 271 5227

**Location:** Plot 635, Akin Adesola Street, Victoria Island, Lagos

**OSINT Value:**
- Landlines harder to spoof than mobile numbers
- "201" Lagos prefix = confirms Nigerian corporate HQ
- Physical address verifiable via Google Maps

#### **2. Toll-Free Numbers**

**Format:** +234 700 XXX XXXX

**Pattern:** "0700" prefix = Nigerian toll-free

**Example:** +234 700 4826 66328

**Special Feature:** Number Spelling
- 0700 4826 66328
- Translates to: 0700 GTBANK
- Marketing technique: Customers dial bank name

**Phoneword Analysis:**
```
G = 4
T = 8
B = 2
A = 2
N = 6
K = 6 (second digit)
```

**Benefits:**
- ✅ Easy to remember
- ✅ Brand reinforcement
- ✅ Reduced customer friction
- ✅ Professional appearance

**OSINT Insight:**
Companies using phonewords typically:
- Large corporations with marketing budgets
- Consumer-facing businesses
- Established brands
- High call volumes

#### **3. Multi-Network Mobile Customer Service**

**Strategy:** Multiple networks for redundancy

**Numbers:**
- +234 802 900 2900 (Airtel - 0802)
- +234 803 900 3900 (MTN - 0803)
- +234 813 985 6000 (MTN - 0813)
- +234 201 448 0000 (Landline backup)

**Pattern Recognition:**

**Airtel:**
- 0802 prefix (older, established)

**MTN:**
- 0803 prefix (older, established)
- 0813 prefix (alternative)

**Network Diversity Strategy:**
- ✅ Not dependent on single network
- ✅ Service continuity if one network fails
- ✅ Wider customer accessibility
- ✅ MTN + Airtel = ~60-70% market coverage

**Redundancy Analysis:**

| Network | Numbers | Purpose |
|---------|---------|---------|
| Airtel | 1 | Primary alternative |
| MTN | 2 | Primary + backup |
| Landline | 1 | Corporate fallback |

**Business Continuity Value:**
If MTN network fails → Customers use Airtel line  
If all mobile networks fail → Landline remains operational

#### **4. WhatsApp-Only Line**

**Number:** +234 904 000 2900 (Airtel - 0904)

**Purpose:** Dedicated WhatsApp customer service

**Significance:**
- Modern digital channel adoption
- Recognizes customer communication preferences
- Separate from voice call infrastructure
- Airtel 0904 = newer prefix (recent allocation)

**OSINT Insight:**
Companies with dedicated WhatsApp lines show:
- Digital transformation awareness
- Customer-centric approach
- Multi-channel strategy
- Modern banking practices

### Hierarchical Phone Structure

**Level 1: Corporate HQ**
- Landlines (201 prefix)
- Official business address
- Highest authority contacts

**Level 2: Customer Service Toll-Free**
- 0700 numbers
- Free for customers
- High-volume support

**Level 3: Mobile Multi-Network**
- 080X, 081X prefixes
- Redundancy strategy
- Accessibility focus

**Level 4: Digital Channels**
- WhatsApp dedicated line
- Modern communication
- Platform-specific support

### Comparative Analysis: MTN vs. GTBank

#### **MTN (Telecommunications Company)**

**Phone Strategy:**
- Uses own network (0903 numbers exclusively)
- Chatbot automation (Zigi)
- Single verified WhatsApp line
- Digital-first approach

**Rationale:**
- Telco can provide own numbers
- Brand reinforcement (use MTN to contact MTN)
- Network quality demonstration
- Cost savings (no competitor network fees)

#### **GTBank (Financial Institution)**

**Phone Strategy:**
- Multiple networks (MTN + Airtel)
- Traditional + modern channels
- Landlines for corporate credibility
- Redundancy prioritized

**Rationale:**
- Banks cannot provide own network
- Reliability critical for financial services
- Diverse customer base across networks
- Backup systems essential

**Key Difference:**
- **MTN:** Single network, digital focus
- **GTBank:** Multi-network, redundancy focus

### Scam Detection Application

**Scenario:** Unknown caller claims to be from GTBank

**Verification Process:**

**Step 1: Check Number Against Official List**

**Legitimate Indicators:** ✅
- Number matches official website
- Landline with 201 prefix (corporate)
- Toll-free 0700 number
- Listed mobile numbers (080X)

**Red Flags:** 🚩
- Unlisted random mobile number
- New prefix (e.g., 091X not on official list)
- International number claiming to be GTBank Nigeria
- Number from wrong network not listed

**Step 2: Number Type Analysis**

| Number Type | Legitimacy Assessment |
|-------------|----------------------|
| **Landline (201)** | ✅ High - Corporate HQ likely legitimate |
| **Toll-Free (0700)** | ✅ High - Customer service likely legitimate |
| **Listed Mobile (080X)** | ⚠️ Medium - Verify on website first |
| **Unlisted Mobile** | 🚩 Low - RED FLAG, potential scam |
| **International (+1, +44, etc.)** | 🚩 Very Low - Nigerian bank unlikely to call from abroad |

**Step 3: Caller Behavior Assessment**

**Scam Indicators:**
- 🚩 Asks for PIN/password
- 🚩 Requests immediate money transfer
- 🚩 Creates urgent/panic situation
- 🚩 Threatens account closure
- 🚩 Asks for personal/financial details

**Legitimate Indicators:**
- ✅ Offers to call back on official line
- ✅ Provides reference number
- ✅ Directs to official channels
- ✅ Never asks for sensitive credentials

**Real-World Value:**

Understanding official phone patterns protects against:
- Vishing (voice phishing)
- Impersonation scams
- Social engineering attacks
- Financial fraud

**Client Service Value:** $50-150 for phone number verification investigation

---

## 💡 KEY INSIGHTS & LESSONS LEARNED

### 1. Phone Numbers Are Intelligence Gateways

**Single 11-digit number reveals:**
- ✅ Mobile network (from prefix)
- ✅ Approximate number age (older vs. newer prefix)
- ✅ Associated businesses (WhatsApp Business)
- ✅ Owner identity (in some cases)
- ✅ Physical locations (GPS coordinates)
- ✅ Contact emails (linked accounts)
- ✅ Websites and social media
- ✅ Business hours and services

**Intelligence Value:**
Phone number = Gateway to complete digital profile

### 2. Google Dorking is Powerful

**Formula Success:**
```
site:[domain] "contact" OR "customer service" "+234"
```

**Why It Works:**
- Bypasses third-party directories
- Direct from authoritative source
- Filters outdated information
- Eliminates scam listings
- Faster than manual navigation

**Best Practices Learned:**
1. Always use `site:` for official numbers
2. Refine for marketplace platforms
3. Cross-verify across multiple pages
4. Check help/contact/about pages
5. Save official numbers for future verification

### 3. WhatsApp Business = Open Intelligence Goldmine

**From Phone Number → Full Business Profile:**

**Step 1:** Save number to contacts  
**Step 2:** Check WhatsApp  
**Step 3:** Access full business information

**Success Rate:** 100% in this investigation (5/5)

**Information Available:**
- Business name, category, description
- Owner names (sometimes)
- Email addresses
- Physical locations with GPS
- Websites and social media
- Product catalogs with pricing
- Operating hours
- Verification status

**Privacy Trade-off:**
Businesses sacrifice privacy for discoverability. OSINT investigators benefit from intentional information sharing.

### 4. Pattern Recognition Reveals Strategy

**Different Organizations = Different Phone Strategies:**

**Banks (GTBank):**
- Landlines + toll-free + multi-network mobile
- Redundancy prioritized
- Traditional + digital channels

**Telcos (MTN):**
- Own network numbers
- Digital-first (chatbots)
- Platform-specific support

**Marketplaces (Jumia):**
- Official corporate + seller numbers
- Requires refinement to distinguish

**Modern Businesses:**
- WhatsApp-dedicated lines
- Digital channel adoption
- Customer communication preferences

**OSINT Application:**
Understanding patterns helps identify legitimate vs. fraudulent contacts.

### 5. Network Prefix = Age & Legitimacy Indicator

**Older Prefixes (080X, 081X):**
- Early 2000s allocation
- More established users/businesses
- Higher perceived credibility
- Often corporate/institutional

**Newer Prefixes (090X):**
- Post-2010 allocation
- Recent subscribers
- Could be new businesses or scammers
- Requires additional verification

**OSINT Insight:**
Scammers often use newer prefixes (easier to acquire). Established businesses typically have older prefixes.

### 6. MTN Dominates Nigerian Business Landscape

**Finding:** 80% of investigated business numbers were MTN

**Possible Reasons:**
- Largest Nigerian network (~40% market share)
- Best infrastructure and coverage
- First-mover advantage in data services
- Business preference for reliability
- Corporate/enterprise services

**OSINT Value:**
Network dominance patterns help profile targets and understand telecommunications landscape.

---

## 🔐 APPLICATIONS FOR SHADOWNODE

### Client Scenario 1: Scam Number Verification

**Problem:** Client received call from number claiming to be their bank, requesting urgent action.

**Solution:**
1. Google Dork official bank numbers (site: operator)
2. Compare caller ID to official list
3. Check number type (landline vs. mobile)
4. Verify prefix matches known bank patterns
5. Provide verdict: Legitimate or Scam

**Deliverable:**
> "Number +234 XXX does NOT appear on official bank contact list. Red flags identified: (1) Mobile number, bank uses landlines for outreach, (2) Unlisted prefix, (3) Caller requested PIN. Assessment: 95% probability SCAM. Recommend: Do not engage, report to bank official channels."

**Value:** Prevented financial fraud, protected client  
**Billing:** $25-50 per number verification

### Client Scenario 2: Business Due Diligence

**Problem:** Client considering partnership with Nigerian business, needs verification.

**Solution:**
1. Investigate company phone numbers via WhatsApp
2. Verify business registration details
3. Check physical location existence (GPS verification)
4. Cross-reference email domains with websites
5. Assess establishment date (account age)
6. Verify network choice matches business claims

**Deliverable:**
Comprehensive business profile:
- Business name and owner
- Physical location (GPS verified)
- Contact methods (email, website)
- Account establishment date
- Legitimacy assessment

**Value:** Risk mitigation, informed decision-making  
**Billing:** $150-300 per business investigation

### Client Scenario 3: Missing Person / Account Recovery

**Problem:** Family needs to locate deceased member's digital accounts/contacts.

**Solution:**
1. Enumerate phone numbers from known devices/records
2. Check WhatsApp for linked accounts
3. Extract email addresses from business profiles
4. Identify social media connections
5. Document all associated digital assets
6. Provide access recovery guidance

**Deliverable:**
Digital estate inventory:
- All phone-linked accounts
- Associated emails and websites
- Social media profiles
- Business/professional accounts

**Value:** Estate management, family closure  
**Billing:** $200-400 per estate investigation

### Client Scenario 4: Corporate Phone Security Audit

**Problem:** Company wants to understand their phone number exposure and security posture.

**Solution:**
1. Enumerate all company phone numbers
2. Check what information is publicly available per number
3. Identify WhatsApp Business information leakage
4. Assess scam/impersonation risk
5. Recommend phone number hygiene practices

**Deliverable:**
Security audit report:
- Complete phone number inventory
- Information exposure per number
- Vulnerability assessment
- Mitigation recommendations
- Best practices guide

**Value:** Security improvement, risk reduction  
**Billing:** $300-600 per corporate audit

### Client Scenario 5: Stalking/Harassment Investigation

**Problem:** Client receiving harassing calls/messages, needs identity of perpetrator.

**Solution:**
1. Check harasser's number on WhatsApp (if business account)
2. Network and prefix analysis (establish patterns)
3. Search number across social media platforms
4. Google Dork for any public associations
5. Document evidence for legal action
6. Provide safety recommendations

**Deliverable:**
Investigation report with:
- Identity information (if available)
- Associated accounts and profiles
- Evidence documentation
- Legal action guidance
- Safety recommendations

**Value:** Personal safety, legal evidence  
**Billing:** $100-250 per harassment investigation

---

## 🎓 SKILLS DEMONSTRATED

- [x] Nigerian phone number format mastery
- [x] Mobile network prefix identification (4 networks)
- [x] Google Dorking for phone intelligence
- [x] WhatsApp Business account investigation
- [x] Information extraction from phone numbers
- [x] Corporate phone pattern analysis
- [x] Scam detection methodology
- [x] Multi-source verification techniques
- [x] Privacy/security assessment
- [x] Business legitimacy verification
- [x] Evidence documentation
- [x] Professional report writing

---

## 🔧 TOOLS USED

### Primary Investigation Tools

| Tool | Purpose | Cost | Rating | Notes |
|------|---------|------|--------|-------|
| **Google Search** | Dorking for official numbers | $0 (Free) | ⭐⭐⭐⭐⭐ | site: operator essential |
| **WhatsApp** | Business account investigation | $0 (Free) | ⭐⭐⭐⭐⭐ | 100% success rate |
| **Chrome Browser** | Research and documentation | $0 (Free) | ⭐⭐⭐⭐⭐ | Standard tool |
| **Company Websites** | Official contact verification | $0 (Free) | ⭐⭐⭐⭐ | Primary source |

### Tools Researched (Not Used)

| Tool | Purpose | Status | Notes |
|------|---------|--------|-------|
| **TrueCaller** | Caller ID & spam detection | Not Available | Will test when accessible |
| **Instagram** | Phone number search | Not Available | Alternative platform |
| **Facebook** | Phone number lookup | Not Available | Alternative platform |
| **Telegram** | Phone-based account search | Not Available | Future investigation |

**Total Investigation Cost:** $0 (All free tools!)

### Alternative Tools to Consider

**For Future Investigations:**
- **TrueCaller** - Crowdsourced caller ID
- **Sync.me** - Reverse phone lookup
- **NumBuster** - Phone number search
- **Spydialer** - US-focused reverse lookup
- **PhoneInfoga** - Advanced phone OSINT framework
- **Telegram** - Username from phone discovery
- **Signal** - Phone-based account check
- **Social media** - Facebook, Instagram phone search

---

## 📊 INVESTIGATION STATISTICS

### Quantified Results

| Metric | Value |
|--------|-------|
| **Investigation Time** | 3 hours |
| **Exercises Completed** | 4 of 5 |
| **Phone Numbers Investigated** | 5 |
| **WhatsApp Success Rate** | 100% (5/5) |
| **Networks Identified** | MTN (80%), Glo (20%) |
| **Emails Discovered** | 100% (5/5) |
| **Physical Locations Found** | 60% (3/5) |
| **Websites Discovered** | 80% (4/5) |
| **Business Names Found** | 100% (5/5) |
| **Google Dorks Successful** | 100% (3/3) |
| **Companies Researched** | 3 (MTN, Jumia, GTBank) |
| **Total Cost** | $0 (free tools) |

### Time Breakdown

| Exercise | Duration | Percentage |
|----------|----------|------------|
| **Exercise 1:** Phone Formats | 30 minutes | 16.7% |
| **Exercise 2:** Google Dorking | 30 minutes | 16.7% |
| **Exercise 3:** TrueCaller Research | Skipped | 0% |
| **Exercise 4:** WhatsApp Investigation | 40 minutes | 22.2% |
| **Exercise 5:** GTBank Analysis | 20 minutes | 11.1% |
| **Documentation & Writing** | 60 minutes | 33.3% |
| **Total** | 180 minutes | 100% |

---

## 📸 EVIDENCE COLLECTED

### Evidence Category 1: WhatsApp Business Profiles

**Number 1: Dawanau Trade Network**
- ✅ Business name screenshot
- ✅ Owner name visible
- ✅ Email and website documented
- ✅ GPS location captured
- ✅ Product catalog screenshots

**Number 2: ChiYa Gadgets**
- ✅ Business profile captured
- ✅ Product catalog screenshots
- ✅ Glo network verified

**Number 3: Zigi (MTN Official)**
- ✅ Verification badge documented
- ✅ Official MTN branding
- ✅ Corporate location verified
- ✅ Cross-referenced with Google Dork

**Number 4: Lifepills**
- ✅ Business information captured
- ✅ Email and website documented
- ✅ Healthcare/wellness category noted

**Number 5: akinjaiyejuoo (Educator)**
- ✅ Profile information captured
- ✅ Account age documented (2017)
- ✅ University affiliation noted
- ✅ Long-term establishment verified

### Evidence Category 2: Google Dork Results

**MTN Nigeria:**
- ✅ Official contact page screenshots
- ✅ Zigi chatbot number verified
- ✅ Multiple support lines documented

**Jumia:**
- ✅ Search results showing multiple numbers
- ✅ Marketplace challenge documented
- ✅ Refinement technique demonstrated

**GTBank:**
- ✅ Complete contact list screenshot
- ✅ All 7 phone categories documented
- ✅ Toll-free phoneword captured
- ✅ Multi-network strategy verified

### Evidence Category 3: Network Analysis

**Prefix Recognition:**
- ✅ All 4 Nigerian networks mapped
- ✅ Prefix lists documented
- ✅ Network distribution calculated (MTN 80%, Glo 20%)

**Pattern Documentation:**
- ✅ Corporate landline patterns (201 prefix)
- ✅ Toll-free structure (0700)
- ✅ Multi-network redundancy strategy
- ✅ WhatsApp-dedicated line identification

---

## ⚖️ LIMITATIONS & DISCLAIMERS

### Investigation Limitations

**Tool Limitations:**
- ⏱️ TrueCaller not available (skipped one exercise)
- 📱 No Instagram/Facebook/Telegram access
- 🔍 WhatsApp only shows Business accounts publicly
- 🌐 Google Dorking finds only indexed pages
- 💾 Deleted accounts leave no trace

**Scope Limitations:**
- 🎯 Small sample size (5 numbers)
- 📍 Nigeria-focused (techniques may vary by country)
- ⏰ 3-hour time constraint
- 🔒 Cannot access private/personal accounts
- 📊 Cannot confirm information freshness

**Technical Limitations:**
- WhatsApp Business profiles only (not personal)
- Publicly shared information only
- No access to telecom databases
- No SIM registration data
- No call detail records (CDRs)

### Ethical & Legal Disclaimer

**This report is for educational and informational purposes only.**

**Ethical Practices Followed:**
- ✅ Only investigated public business numbers
- ✅ All information was publicly shared by businesses
- ✅ No unauthorized access attempted
- ✅ Respected WhatsApp privacy settings
- ✅ Used findings for learning, not harm
- ✅ Understood legal boundaries

**Did NOT:**
- ❌ Investigate private individuals without cause
- ❌ Attempt to bypass privacy settings
- ❌ Share sensitive personal findings publicly
- ❌ Use techniques for harassment or stalking
- ❌ Attempt SIM swapping or cloning
- ❌ Hack into accounts or systems

**Legal Considerations:**

**Phone Number OSINT is Legal When:**
- Using publicly available information
- No unauthorized access to systems
- Not violating platform terms of service
- Not used for harassment or stalking
- Complying with local privacy laws

**Phone Number OSINT is Illegal When:**
- SIM cloning/swapping
- Accessing telecom databases without authorization
- Phone hacking or interception
- Harassment or stalking
- Violating wiretapping laws
- Identity theft purposes

**Privacy Awareness:**
This investigation demonstrates that phone numbers reveal significant information. Users should:
- Be cautious about sharing numbers publicly
- Understand WhatsApp Business privacy settings
- Review what information is publicly visible
- Consider separate business/personal numbers

---

## 💡 LESSONS LEARNED - DEEP DIVE

### Technical Lessons

**1. Phone Number Structure = First Layer Intelligence**

Understanding format reveals:
- Country of origin (country code)
- Mobile vs. landline (prefix patterns)
- Network provider (Nigerian prefixes)
- Approximate age (older vs. newer prefixes)
- Geographic location (landline area codes)

**Application:**
Before any tool usage, phone number itself provides context.

**2. Google Dorking Cuts Through Noise**

**Problem:** Generic Google searches return:
- Outdated directories
- Third-party listings
- Scam numbers
- Spam sites

**Solution:** `site:` operator
```
site:official-domain.com "contact" "+234"
```

**Result:**
- Direct from authoritative source
- Current information
- No third-party pollution
- Official verification

**3. WhatsApp Business = Intentional Information Sharing**

**Key Insight:**
Businesses WANT to be found. They intentionally share:
- Names, emails, locations
- Operating hours, products
- Owner information (sometimes)

**OSINT Advantage:**
No "hacking" required. Information freely provided for marketing purposes.

**Ethical Consideration:**
Using publicly shared information = Legal and ethical

**4. Cross-Verification Multiplies Confidence**

**Example: MTN Zigi Chatbot**
- Found via Google Dork (Exercise 2)
- Verified via WhatsApp (Exercise 4)
- Blue checkmark confirmation
- Official website cross-reference

**Result:** 100% confidence in legitimacy

**Best Practice:**
Never rely on single source. Multiple confirmations = higher certainty.

**5. Pattern Recognition Enables Prediction**

After analyzing GTBank's phone strategy:
- Can predict structure for other banks
- Identify anomalies (potential scams)
- Understand industry standards
- Spot deviations from norm

**Example Application:**
New bank claims to only have mobile numbers → Red flag (banks use landlines)

### Investigative Lessons

**1. Phone Numbers Are Identity Anchors**

**Phone number connects to:**
- Social media accounts
- Email addresses
- Physical locations
- Business registrations
- Online profiles

**Intelligence Value:**
Single number = Gateway to entire digital identity

**2. Network Choice Indicates Business Maturity**

**MTN (80% of sample):**
- Most established network
- Premium pricing
- Business preference
- Reliability focus

**Other Networks:**
- Cost-sensitive businesses
- Regional preferences
- Newer companies

**OSINT Insight:**
Network selection can indicate business priorities and maturity.

**3. Account Age = Credibility Indicator**

**Example: akinjaiyejuoo (2017 account)**
- 8+ years established
- Long-term presence
- Higher legitimacy probability

**Scammers typically:**
- Use recently acquired numbers
- New accounts (days/weeks old)
- Disposable numbers

**Verification Technique:**
Check WhatsApp "joined" date or account establishment

**4. Information Leakage is Asymmetric**

**Business Accounts:**
- Intentionally share everything
- Marketing > privacy
- Want to be discovered

**Personal Accounts:**
- More privacy-conscious
- Limited public information
- Harder to investigate

**OSINT Strategy:**
Business investigations easier than personal investigations

**5. Redundancy Reveals Importance**

**GTBank's Multi-Network Strategy:**
Shows that phone accessibility is:
- Mission-critical for banks
- Worth additional cost
- Risk mitigation priority

**OSINT Application:**
Organizations with redundant numbers take customer service seriously (or have been victims of outages).

### Practical Takeaways

**For Future Investigations:**

**✅ Always Start With:**
1. Phone number format analysis
2. Network identification
3. Google Dorking official sources
4. WhatsApp Business check
5. Cross-verification

**✅ Document Everything:**
1. Screenshots of all findings
2. Timestamps of searches
3. URLs of sources
4. Cross-references
5. Confidence levels

**✅ Be Ethical:**
1. Only investigate with legitimate purpose
2. Respect privacy settings
3. Don't harass or stalk
4. Use information responsibly
5. Understand legal boundaries

**🚩 Red Flags to Watch:**

**In Phone Numbers:**
- Recently acquired (days/weeks old)
- Newer prefixes (090X) claiming established business
- Mismatched network claims
- International numbers for local businesses
- No online presence whatsoever

**In WhatsApp Profiles:**
- Generic business names
- No physical location
- No email or website
- Recently created accounts
- Poor grammar in descriptions
- Stock photos as logos

**In Official Contacts:**
- Not listed on company website
- Different from known patterns
- Requests sensitive information
- Creates urgency/panic
- Threatens account closure

---

## 🔄 RELATED INVESTIGATIONS

- **Day 25:** ChatGPT.com domain intelligence
- **Day 19:** Username enumeration (Davido)
- **Day 12:** Tesla corporate intelligence
- **Day XX:** Reverse image search investigation
- **Future:** Email OSINT investigation
- **Future:** Social media phone number linking

---

## 🎯 NEXT STEPS & FUTURE INVESTIGATIONS

### Immediate Applications

**✅ Skills to Practice:**
- [ ] Test TrueCaller when available
- [ ] Investigate international phone numbers
- [ ] Try phone OSINT on different countries
- [ ] Build phone number database
- [ ] Create scam number verification service

**✅ Tool Mastery:**
- [ ] **PhoneInfoga** - Advanced OSINT framework
- [ ] **Holehe** - Email to phone discovery
- [ ] **Maigret** - Username to phone linking
- [ ] **Social media** - Phone search features
- [ ] **Telegram** - Phone-based account discovery

### Advanced Skill Development

**📈 Next Level Techniques:**
- [ ] Automated phone enumeration
- [ ] SIM card investigation (legal methods)
- [ ] Call spoofing detection
- [ ] Phone number clustering analysis
- [ ] Carrier lookup APIs
- [ ] Phone validation services
- [ ] International format conversion
- [ ] Phone history tracking

### Service Development

**💼 ShadowNode Offerings:**
- [ ] **Basic Number Verification:** $25-50
- [ ] **Business Due Diligence:** $150-300
- [ ] **Corporate Security Audit:** $300-600
- [ ] **Harassment Investigation:** $100-250
- [ ] **Scam Detection Service:** $50-150

---

## 📚 RESOURCES & REFERENCES

### Primary Sources

**1. Company Websites:**
- MTN Nigeria: mtn.ng
- Jumia: jumia.com.ng
- GTBank: gtbank.com/help-centre

**2. Investigation Tools:**
- Google Search (Dorking)
- WhatsApp Messenger
- Chrome Browser

**3. Network Information:**
- Nigerian Communications Commission (NCC)
- Mobile network prefix databases
- Telecommunications industry reports

### Secondary Sources

**4. WhatsApp Business:**
- business.whatsapp.com
- Business profile features
- Public information sharing

**5. Google Dorking:**
- Advanced search operators
- Site-specific search techniques
- Contact information discovery

**6. TrueCaller (Research):**
- truecaller.com
- Crowdsourced caller ID
- Spam detection features

### Date of Investigation

**All data collected on:** November 11, 2025  
**Location:** Kogi State, Nigeria  
**Duration:** 3 hours (180 minutes)

---

## 🌟 PERSONAL REFLECTION

### What Surprised Me Most

**Phone Numbers = Intelligence Goldmines**

Before this investigation, I thought phone numbers were just contact information. Now I understand they're:
- Identity anchors
- Business profile gateways
- Network indicators
- Age/establishment signals
- Location markers

**WhatsApp Business Transparency**

The extent of public information sharing shocked me:
- Owner names visible
- GPS coordinates provided
- Complete business profiles
- Product catalogs accessible

Businesses sacrifice privacy for discoverability. As an OSINT investigator, I benefit from their marketing needs.

### Most Valuable Skill Learned

**Google Dorking with site: operator**

This single technique:
- Cuts through search noise instantly
- Finds official information directly
- Eliminates outdated/scam results
- Saves enormous time

**Formula:**
```
site:[official-domain] "contact" "+234"
```

This will be foundational for all future investigations.

### Biggest Challenge

**TrueCaller Not Available**

Not having TrueCaller access limited investigation scope. However, this forced creativity:
- Relied on WhatsApp as alternative
- Researched tool capabilities theoretically
- Achieved 100% success with available tools

**Lesson:** Work with what you have. Free tools (Google, WhatsApp) provided comprehensive intelligence.

### Mom's Blessing at Work

**Every tool used: FREE**
- Google Search: $0
- WhatsApp: $0
- Chrome Browser: $0
- Company Websites: $0

**Total Cost: $0**

No expensive OSINT platforms needed. Public information + creative thinking = Professional-grade intelligence.

This proves that financial constraints don't limit OSINT capabilities. Information is out there, freely accessible to anyone willing to look.

### Real-World Application

This investigation taught me practical skills I can offer clients:
- Scam number verification
- Business legitimacy checks
- Contact discovery
- Due diligence investigations

Each service has clear dollar value ($25-600 range). Phone number OSINT is a marketable skill.

---

## 📝 ABOUT THIS INVESTIGATION

**Purpose:** Self-directed learning project as part of 90-day OSINT skill development

**Goal:** Master phone number intelligence techniques applicable to Nigerian telecommunications and business verification.

**Future Work:** This investigation establishes foundation for:
- International phone OSINT
- Advanced carrier analysis
- Automated phone enumeration
- Scam detection services
- Business verification offerings

**Investigation Type:** Phone Number Intelligence & Business Verification

**Difficulty Level:** Beginner to Intermediate

**Reproducibility:** High (all tools free and accessible)

**Practical Value:** Essential skill for modern investigations and personal security

**Geographic Focus:** Nigeria (techniques adaptable to other regions)

---

## ✍️ REPORT METADATA

**Report Prepared By:** Joy Ewatomi  
**Agency:** ShadowNode Intelligence Agency  
**Date:** November 11, 2025  
**Day:** 22 of 90-Day Journey  
**Location:** Kogi State, Nigeria  
**Report Version:** 1.0  
**Classification:** Public / Educational  
**Quality Assurance:** Multi-source verification completed  
**Currency Updated:** Dollar values used for billing estimates

---

**Case Status:** ✅ CLOSED  
**Confidence Level:** High (90%+ on methodologies)  
**Documentation Quality:** Comprehensive  
**Reproducible:** Yes  
**Evidence Preserved:** ✅ Complete  
**Success Rate:** 100% (WhatsApp), 100% (Google Dorking)

**Investigator Signature:**  
Joy Ewatomi  
ShadowNode Intelligence Agency  
Day 22 of 90-Day Journey  

*"Operating from the shadows to bring truth to light"* 🔐

---

## 📱 SOCIAL MEDIA

**LinkedIn Post Draft:**

> 📞 **OSINT Case Study: Phone Number Intelligence Investigation - Nigeria**
> 
> Just completed a 3-hour deep-dive into phone number OSINT. The results shocked me.
> 
> **From a single phone number, I discovered:**
> 
> ✅ Full business names (100% success rate)  
> ✅ Email addresses (100% - 5 out of 5 numbers)  
> ✅ Physical locations with GPS coordinates (60%)  
> ✅ Websites and social media (80%)  
> ✅ Owner names, products, operating hours  
> ✅ Business establishment dates (credibility indicators)
> 
> **Tools Used:** Google, WhatsApp. **Total Cost:** $0
> 
> **Key Findings:**
> 
> 🔍 **Google Dorking Power**  
> Formula: `site:company.com "contact" "+234"`  
> Bypasses spam, finds official numbers instantly
> 
> 💬 **WhatsApp Business = Intelligence Goldmine**  
> Businesses want to be found → They share EVERYTHING  
> Phone number = gateway to complete business profile
> 
> 📊 **MTN Dominates Nigerian Business**  
> 80% of investigated numbers were MTN network  
> Network choice indicates business priorities
> 
> 🛡️ **Scam Detection Application**  
> Know official phone patterns → Spot fraudulent callers  
> GTBank uses landlines (201) + toll-free (0700) + multi-network mobile  
> Random unlisted mobile claiming to be bank? RED FLAG 🚩
> 
> **Real-World Value:**
> - Scam verification: $25-50
> - Business due diligence: $150-300
> - Corporate security audit: $300-600
> 
> **Biggest Lesson:** Phone numbers aren't just contact info—they're identity anchors revealing entire digital footprints.
> 
> All with FREE tools. No expensive platforms needed.
> 
> Day 22 of my 90-day journey mastering Open Source Intelligence.
> 
> #OSINT #PhoneIntelligence #CyberSecurity #ScamPrevention #BusinessVerification #Nigeria #ShadowNode #TelecommunicationsIntelligence

**Hashtags:**  
#OSINT #Day22of90 #CyberSecurity #PhoneOSINT #ScamDetection #BusinessIntelligence #Nigeria #WhatsAppBusiness #GoogleDorking #ShadowNode #OpenSourceIntelligence #InvestigativeJournalism #Telecommunications #FraudPrevention

---

## 🎁 BONUS: QUICK REFERENCE GUIDE

### "Phone Number OSINT in 15 Minutes" Cheat Sheet

**🎯 Objective:** Verify phone number legitimacy and extract intelligence

**⚡ Quick Start Process:**

**Step 1: Format Analysis (2 minutes)**
1. Identify country code (+234 = Nigeria)
2. Determine network from prefix
3. Assess age (080X = older, 090X = newer)

**Step 2: Google Dorking (5 minutes)**
1. Determine if business/corporate number
2. Google Dork: `site:company.com "contact" "[phone]"`
3. Check if number appears on official website
4. Verify phone number type (landline/mobile)

**Step 3: WhatsApp Check (5 minutes)**
1. Save number to contacts
2. Open WhatsApp and search
3. If Business account exists:
   - View full profile
   - Screenshot all information
   - Note: name, email, location, website
4. Check verification badges

**Step 4: Assessment (3 minutes)**
1. Compare findings across sources
2. Look for consistency/inconsistencies
3. Assign confidence level
4. Document verdict: Legitimate / Suspicious / Scam

**⏱️ Total Time:** 15 minutes  
**💰 Cost:** $0 (Free)  
**✅ Effectiveness:** High for business numbers

---

### Nigerian Phone Number Quick Reference

**Format:** +234 XXX XXX XXXX (or 0XXX XXX XXXX domestic)

**Network Identification:**
- **080X, 081X, 090X** = Check second digit:
  - X = 2 (Airtel), 3 (MTN), 5 (Glo), 6 (MTN), 7 (varies), 9 (9mobile)

**Landline Patterns:**
- **01** = Lagos (old)
- **201** = Lagos (new)
- **0700** = Toll-free

**Red Flags:**
- 🚩 Very new number claiming established business
- 🚩 Network mismatch with company claims
- 🚩 Not listed on official company website
- 🚩 Requests sensitive information
- 🚩 No WhatsApp Business account (for claimed business)

---

*Phone number OSINT is a fundamental investigative skill. In Nigeria, where WhatsApp Business is ubiquitous, phone numbers are gateways to comprehensive business intelligence. Understanding this landscape protects both investigators and citizens from fraud while enabling legitimate due diligence.*

**END OF REPORT**
