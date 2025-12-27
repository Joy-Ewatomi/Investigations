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

