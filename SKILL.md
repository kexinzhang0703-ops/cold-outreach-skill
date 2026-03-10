---
name: cold-outreach
description: >
  Professional networking and job search outreach system for LinkedIn messages, recruiter emails, 
  coffee chat coordination, and follow-ups. Use when the user needs to: (1) Write LinkedIn connection 
  requests or messages to professionals, alumni, recruiters, or hiring managers, (2) Draft emails to 
  recruiters about job opportunities, (3) Coordinate or prepare for coffee chats and informational 
  interviews, (4) Write follow-up messages after networking events or conversations, (5) Plan outreach 
  strategy or ask for networking advice. Triggers include phrases like "reach out to", "LinkedIn message", 
  "contact recruiter", "coffee chat", "networking email", "follow up with", or any request involving 
  professional networking communication.
---

# Cold Outreach

Professional networking communication system trained on multiple social media cold outreach email templates and real-world examples. This skill provides AI-powered message generation for LinkedIn and email outreach.

## Core Training Sources

This skill synthesizes best practices from:
- Multiple LinkedIn message templates optimized for 300-character limit
- Cold email examples from successful job seekers
- Recruiter outreach strategies
- Coffee chat coordination workflows
- Professional networking frameworks

## Essential First-Time Setup

**CRITICAL**: When a user triggers this skill for the first time, Claude MUST:

1. **Request Resume Upload**
   ```
   "To write the most effective outreach messages, I'll need your resume. 
   Please upload your CV/resume so I can tailor messages based on your 
   background and experience."
   ```

2. **Wait for Resume**
   - Do not proceed without the resume
   - Parse resume for: background, skills, experience, education, current goals
   - Store key information for message personalization

## 🔄 Standard Workflow (Every Outreach Request)

### Step 1: Collect Recipient Information

Ask the user to provide the following information about the person:

```
"Please paste the following information about the person you want to reach out to:

1. **Name and Current Position**: [Full name and job title]
2. **Company**: [Where they work now]
3. **Work Experience**: [Brief background - you can copy from their LinkedIn]
4. **Your Relationship**: 
   - Alumni (same school)
   - Former colleague
   - Current colleague
   - Same company (different team)
   - No existing relationship
   - Other: [specify]
"
```

**Important**: Wait for user to provide this information before proceeding.

### Step 2: Choose Message Format

Present the user with format options:

```
"What type of message would you like me to write?

1. **LinkedIn Message** (300 characters max - for connection requests or InMail)
2. **Email** (No length limit - more detailed introduction)

Please select 1 or 2."
```

### Step 3: Determine Opening Strategy

Based on the relationship information provided:

**If there IS a relationship** (alumni/colleague/etc):
- Lead with the connection point
- Examples:
  - "Hi [Name], I noticed we're both [School] alums..."
  - "Hi [Name], I saw you're also at [Company]..."
  - "Hi [Name], I remember working together at [Company]..."

**If there is NO relationship**:
- Default to expressing interest in their company/role
- Template logic:
  ```
  "Hi [Name],
  
  I came across your profile and was really impressed by your work at [Company]. 
  I'm particularly interested in [their role/department/company mission], and 
  I'd love to connect and learn from your experience."
  ```

### Step 4: Generate Personalized Message

Using the collected information:

1. **Extract from user's resume**:
   - Relevant experience that matches recipient's field
   - Skills that align with recipient's company/role
   - Career goals that connect to recipient's path

2. **Extract from recipient's information**:
   - Current role and company
   - Notable experiences or achievements
   - Industry/field

3. **Craft opening based on relationship**:
   - If relationship exists: Lead with connection point
   - If no relationship: Express interest in their company/role

4. **Add value proposition** (from user's resume):
   - Relevant background
   - Shared interests/industry
   - Clear, specific ask

5. **Keep within format constraints**:
   - LinkedIn: Maximum 300 characters
   - Email: 100-200 words (concise but complete)

## Message Generation Rules

### For LinkedIn Messages (300 characters max)

**Structure**:
1. Greeting + connection point or interest statement (1 sentence)
2. Brief self-introduction with relevant credential (1 sentence)
3. Specific ask (1 sentence)

**Character-saving tips**:
- Use contractions ("I'm" not "I am")
- Remove filler words
- Use pronouns after first mention
- Keep names short (first name only after greeting)

**Example** (Alumni):
```
Hi Sarah, I'm also a Stanford alum exploring tech PM roles. I saw your work 
at Google and would love to learn from your experience. Would you have 20 
minutes for a quick chat?
```

**Example** (No relationship - Company interest):
```
Hi Michael, I'm very interested in the AI initiatives at DeepMind and your 
work in reinforcement learning. I'd love to connect and learn about your 
journey. Open to a brief chat?
```

### For Email Messages (Longer format)

**Structure**:
1. Subject line (if email)
2. Greeting + connection/interest statement
3. 2-3 sentences about user's background (from resume)
4. Specific interest in recipient's work/company
5. Clear ask with time frame
6. Professional closing

**Length**: 100-200 words total

**Example** (Alumni):
```
Subject: Fellow Berkeley Alum - Coffee Chat Request

Hi David,

I noticed you're a UC Berkeley alum working as a Product Manager at Stripe. 
I'm currently transitioning from consulting into product roles and would 
love to learn from someone who's successfully made a similar move.

I have 3 years of experience at McKinsey working on digital transformation 
projects, and I'm particularly drawn to fintech companies like Stripe that 
are reshaping financial infrastructure.

Would you have 20-30 minutes in the next two weeks for a coffee chat? I'd 
love to hear about your experience at Stripe and get your advice on breaking 
into product management.

Happy to work around your schedule!

Best,
[User's name]
```

**Example** (No relationship - Company/role interest):
```
Subject: Exploring Opportunities in AI Research

Hi Dr. Chen,

I came across your profile and was really impressed by your work on multimodal 
learning at OpenAI. I'm particularly interested in the research your team is 
doing on vision-language models.

I recently completed my PhD in Computer Vision at MIT, focusing on self-supervised 
learning methods. My dissertation work on contrastive learning has strong 
parallels to some of the approaches your team has published.

I'd love to connect and learn more about the research culture at OpenAI and 
potential opportunities to contribute. Would you be open to a brief 20-minute 
conversation?

Thank you for considering!

Best,
[User's name]
```

## 🎨 Customization Based on Relationship Type

### Alumni Connection
- **Opening**: "I noticed we're both [School] alums..."
- **Connection**: Shared educational background
- **Ask**: "Would love to learn from a fellow [School mascot/name]"

### Former/Current Colleague
- **Opening**: "I remember working together at [Company]..." or "I saw we're both at [Company]..."
- **Connection**: Shared work experience
- **Ask**: More casual, can reference shared context

### Same Industry/Field
- **Opening**: "I noticed your work in [field]..."
- **Connection**: Shared professional interests
- **Value**: Highlight parallel experience from user's resume

### No Relationship (Default)
- **Opening**: "I was really impressed by [their company/role/work]..."
- **Interest**: "I'm particularly interested in [specific aspect]..."
- **Ask**: "I'd love to connect and learn from your experience..."

## Additional Scenarios

### Coffee Chat Coordination
- Follow the templates in `references/coffee-chat-guide.md`
- Initial request → Scheduling → Reminder → Follow-up

### Recruiter Outreach
- See `references/recruiter-strategy.md` for approach
- Always attach resume when emailing recruiters
- Reference specific job posting if applying to one

### Follow-up Messages
- Reference specific conversation points
- Show action taken based on their advice
- Maintain relationship without asking for favors

## Technical Implementation Notes

**Resume Parsing**:
- Extract: Name, current role, education, skills, experience highlights
- Identify: Industry, target roles, key achievements
- Store: For use across multiple outreach messages

**Relationship Detection**:
- Parse user input for relationship keywords
- Default to "no relationship" if unclear
- Always confirm relationship type before generating

**Format Enforcement**:
- LinkedIn: Hard limit at 300 characters
- Email: Soft target of 100-200 words
- Always count characters/words before output

**Personalization Engine**:
1. Match user's background (resume) to recipient's field
2. Find relevant connection points
3. Craft authentic interest statement
4. Create specific, time-bounded ask

## 📖 Resources

- **references/templates.md**: All message templates organized by scenario
- **references/coffee-chat-guide.md**: Complete coffee chat SOP from request to follow-up
- **references/recruiter-strategy.md**: Why recruiters matter, how to find them, outreach volume strategy

## 🚫 What to Avoid

- Apologetic language ("sorry to bother")
- Vague requests ("pick your brain")
- Life story or job search complaints
- Multiple questions in initial message
- Generic praise without specifics
- Excessive formality or casualness
