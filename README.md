# Cold Outreach Skill for Claude

A professional networking and job search outreach system designed as a custom skill for Claude AI. This skill is trained on multiple cold outreach email templates and real-world examples from social media, optimized for both LinkedIn messages (300 characters) and longer email formats.

## What This Skill Does

This skill helps you craft professional, effective outreach messages for:

- **LinkedIn Connection Requests & Messages**: Optimized for the 300-character limit
- **Cold Emails**: Longer, more detailed professional introductions
- **Recruiter Outreach**: Job-specific applications and general exploration
- **Coffee Chat Coordination**: From initial request to follow-up
- **Follow-up Messages**: Post-meeting relationship maintenance

## Key Features

- **Resume-Based Personalization**: Upload your resume once, get tailored messages for every outreach
- **Smart Relationship Detection**: Automatically adapts opening based on your connection (alumni, colleague, or no relationship)
- **Dual Format Support**: 
  - LinkedIn Messages (≤300 characters)
  - Full Emails (100-200 words)
- **Intelligent Opening Strategy**: 
  - If you have a connection → Leads with that
  - If no connection → Expresses interest in their company/role
- **Comprehensive Templates**: Covers all major networking scenarios

## How to Use

### First-Time Setup

1. When you first use this skill, Claude will ask you to upload your resume
2. Your resume is parsed to extract:
   - Professional background
   - Skills and experience
   - Education
   - Career goals

### Standard Workflow

For each outreach message:

**Step 1**: Provide recipient information
- Name and current position
- Company
- Work experience (copy from LinkedIn)
- Your relationship to them (alumni/colleague/none/etc.)

**Step 2**: Choose message format
- LinkedIn Message (300 characters max)
- Email (longer format)

**Step 3**: Claude generates a personalized message
- Uses your resume for relevant background
- Adapts opening based on relationship
- Stays within character limits
- Creates a specific, actionable ask

### Example Use Cases

**Scenario 1: Reaching out to an alumni**
```
Input: 
- Name: Sarah Chen
- Position: Product Manager at Google
- Relationship: Stanford alumni

Output: LinkedIn message that leads with "Fellow Stanford alum" 
and highlights relevant PM experience from your resume
```

**Scenario 2: Cold outreach (no connection)**
```
Input:
- Name: Michael Rodriguez
- Position: AI Research Scientist at DeepMind  
- Relationship: None

Output: Message expressing genuine interest in DeepMind's AI work
and connecting your background to their research area
```

## What Makes This Different

### Traditional Cold Email
- Generic templates
- Manual customization
- No context awareness
- Same message to everyone

### This Skill
- AI-powered personalization
- Resume-aware matching
- Relationship-based opening
- Company/role-specific interest
- Format-optimized (LinkedIn vs Email)

## Included Resources

This skill comes with comprehensive reference guides:

- **`templates.md`**: 20+ message templates for every scenario
- **`coffee-chat-guide.md`**: Complete SOP for informational interviews
- **`recruiter-strategy.md`**: How to find and approach recruiters

## 🎨 Message Examples

### LinkedIn Message (Alumni)
```
Hi Sarah, I'm also a Stanford alum exploring tech PM roles. I saw your 
work at Google and would love to learn from your experience. Would you 
have 20 minutes for a quick chat?
```
*Character count: 184/300*

### Email (No Relationship)
```
Subject: Exploring Opportunities in AI Research

Hi Dr. Chen,

I came across your profile and was really impressed by your work on 
multimodal learning at OpenAI. I'm particularly interested in the research 
your team is doing on vision-language models.

I recently completed my PhD in Computer Vision at MIT, focusing on 
self-supervised learning methods. My dissertation work on contrastive 
learning has strong parallels to some of the approaches your team has 
published.

I'd love to connect and learn more about the research culture at OpenAI 
and potential opportunities to contribute. Would you be open to a brief 
20-minute conversation?

Thank you for considering!

Best,
[Your name]
```

## Installation

### For Claude.ai Users

1. Download this repository
2. Navigate to Claude.ai Settings → Custom Skills
3. Upload the entire `cold-outreach-skill` folder
4. The skill will automatically activate when you use trigger phrases like:
   - "Write a LinkedIn message to..."
   - "Draft a cold email to..."
   - "Help me reach out to..."

### For Claude API Users

1. Include the `SKILL.md` content in your system prompt
2. Reference the skill documentation when needed
3. Follow the workflow specified in the skill file

## 📖 Documentation

- **[SKILL.md](SKILL.md)**: Complete skill instructions and workflow
- **[references/templates.md](references/templates.md)**: All message templates
- **[references/coffee-chat-guide.md](references/coffee-chat-guide.md)**: Coffee chat SOP
- **[references/recruiter-strategy.md](references/recruiter-strategy.md)**: Recruiter outreach strategy

## Contributing

Contributions are welcome! If you have:
- Additional cold outreach templates that work well
- Improvements to message generation logic
- New networking scenarios to cover
- Bug fixes or enhancements

Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

This skill was developed by synthesizing best practices from:
- Multiple social media cold outreach templates
- Real-world job search success stories
- Professional networking experts
- LinkedIn message optimization research

## ⚠️ Best Practices

**DO:**
- Upload your updated resume for best results
- Provide specific information about the recipient
- Choose the right format (LinkedIn vs Email)
- Customize the generated message if needed
- Follow up appropriately (see coffee-chat-guide.md)

**DON'T:**
- Use the same generic message for everyone
- Apologize for reaching out
- Make vague requests ("pick your brain")
- Send overly long LinkedIn messages
- Forget to personalize with specific details

## Success Metrics

This skill is optimized for:
- **Response Rate**: Messages follow proven templates with high response rates
- **Time Efficiency**: Generate personalized messages in seconds vs. hours
- **Consistency**: Maintain professional tone across all messages
- **Relevance**: Resume-based matching ensures you highlight the right experience

## 🔮 Future Enhancements

Planned features:
- [ ] Multi-language support (Mandarin, Spanish, etc.)
- [ ] Industry-specific templates (tech, finance, consulting)
- [ ] A/B testing suggestions
- [ ] Response analysis and optimization
- [ ] Integration with LinkedIn API

## 📬 Contact

If you have questions or feedback about this skill, please open an issue on GitHub.

---

**Note**: This is a custom skill for Claude AI. It requires Claude's context window and instruction-following capabilities to work effectively.
