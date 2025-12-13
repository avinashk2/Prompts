# Time-Adaptive LLM Course Generator

You are an expert instructional designer. Create a comprehensive course outline for **[TOPIC]** that is designed exclusively for learning through LLM conversations, optimized to be completed in **[TIME_HOURS] hours**.

## Course Parameters (USER INPUTS)
- **Topic**: [TOPIC]
- **Time Available**: [TIME_HOURS] hours
- **Starting Level**: [BEGINNER/INTERMEDIATE/ADVANCED]

---

## Dynamic Level-Based Adaptations

### Content Complexity by Starting Level

**BEGINNER Level Adjustments:**
- Assume ZERO prior knowledge of [TOPIC]
- Start with fundamental definitions and "why this matters"
- Use simple, everyday analogies and examples
- Include more foundational questions (20-30% more time on basics)
- Avoid jargon or always define technical terms immediately
- Break complex concepts into smaller sub-questions
- Include more verification and "check your understanding" points
- Questions should be: "Explain X as if I've never heard of it, with simple examples..."

**INTERMEDIATE Level Adjustments:**
- Assume basic familiarity with [TOPIC] fundamentals
- Skip introductory "what is" questions, start with "how to"
- Use technical terminology without extensive definitions
- Focus more on application and best practices (40-50% of time)
- Include comparison questions: "Compare X vs Y approaches..."
- Questions should be: "Show me how to implement X and explain when to use different approaches..."
- Reduce foundational content by 30-40%

**ADVANCED Level Adjustments:**
- Assume solid working knowledge of [TOPIC]
- Skip fundamentals entirely, jump to advanced techniques
- Focus on optimization, edge cases, and complex scenarios (60-70% of time)
- Include architecture and design pattern questions
- Deep dive into "why" and trade-offs rather than "what"
- Questions should be: "Explain the trade-offs between X and Y in production scenarios..."
- Include performance, scalability, and advanced troubleshooting

### Phase Naming Convention by Level
- **Beginner**: "Understanding [Concept]", "Introduction to [Topic]"
- **Intermediate**: "Implementing [Feature]", "Working with [Tool]"
- **Advanced**: "Optimizing [System]", "Advanced [Technique] Patterns"

---

## Automatic Time-Based Scaling

### Calculate Course Structure Based on Time Input

**For [TIME_HOURS] hours, automatically generate:**

1. **Number of Phases**: 
   - 1-3 hours → 2-4 phases (sprint learning)
   - 4-8 hours → 5-8 phases (focused course)
   - 9-16 hours → 9-14 phases (standard course)
   - 17-30 hours → 15-20 phases (comprehensive course)
   - 30+ hours → 20-25 phases (deep mastery)

2. **Points per Phase**:
   - Sprint (1-3h): 2-3 questions per phase
   - Focused (4-8h): 3-4 questions per phase
   - Standard (9-16h): 4-5 questions per phase
   - Comprehensive (17-30h): 4-6 questions per phase
   - Deep (30+h): 5-7 questions per phase

3. **Time per Conversation**:
   - Quick concept: 8-12 minutes
   - Standard learning: 12-18 minutes
   - Deep dive: 18-25 minutes
   - Practice session: 15-20 minutes

4. **Depth Level** (adjust based on time):
   - <5 hours: Essential concepts only, minimal practice
   - 5-10 hours: Core concepts + guided practice
   - 10-20 hours: Core + intermediate + hands-on practice
   - 20-40 hours: Comprehensive + advanced topics + projects
   - 40+ hours: Complete mastery + edge cases + real-world applications

### Time Estimate Adjustment Factors

**Question Complexity Multipliers:**
- Simple explanation: 1.0x base time (10-12 min)
- Explanation + examples: 1.3x base time (13-16 min)
- Explanation + examples + practice: 1.5x base time (15-18 min)
- Step-by-step guidance + troubleshooting: 1.8x base time (18-22 min)
- Complex problem-solving + multiple scenarios: 2.0x base time (20-25 min)

**Starting Level Time Adjustments:**
- **Beginner**: Add 20% to all time estimates (more reading, processing time)
- **Intermediate**: Use base time estimates as-is
- **Advanced**: Reduce by 10% (faster comprehension, less explanation needed)

**Response Length Considerations:**
- Short answer expected (<500 words): 8-12 min
- Standard answer (500-1000 words): 12-18 min
- Comprehensive answer (1000-1500 words): 18-22 min
- Extensive answer with multiple examples (1500+ words): 22-25 min

**Buffer Time Allocation:**
- Reserve 15-20% of total time for:
  - Re-reading complex responses
  - Asking clarifying follow-up questions
  - Taking notes or mental processing breaks
  - Reviewing previous concepts when needed

---

## LLM-Only Learning Requirements

### 1. Self-Contained Learning Points
- Each point must be completely explainable by an LLM in one conversation
- Include all necessary context, examples, and practice exercises
- No references to external documentation, websites, or tutorials
- Each point generates a complete mini-lesson

### 2. Conversation-Ready Questions
Each question must prompt the LLM to provide:
- Clear explanation with examples
- Step-by-step instructions (when applicable)
- Practice exercises within the conversation
- Common mistakes to avoid
- How to verify understanding

### 3. Progressive Complexity
- Start with conceptual understanding through LLM explanations
- Move to LLM-guided practice exercises
- Progress to LLM-assisted problem solving
- End with LLM-supported real-world application (if time permits)

---

## Question Format Guidelines

### Effective LLM Learning Questions

✅ **Good Examples**:
- "Explain [concept] with 3 practical examples and help me understand when to use it" (⏱️ 12 min)
- "Show me how to [action] step-by-step with an example" (⏱️ 15 min)
- "Guide me through [process], explain potential pitfalls, and help me practice" (⏱️ 20 min)

❌ **Avoid**:
- Vague questions: "Learn about X"
- External dependencies: "Read this article"
- Tool requirements without context: "Install X and try it"

### Question Structure Template
"[Action verb] + [specific topic] + [request for examples/guidance] + [practice/verification]"

---

## Time-Optimized Content Strategy

### For SHORT courses (1-5 hours):
- Focus on **essential concepts only**
- Minimal practice exercises
- Surface-level coverage
- "Understand what it is and when to use it"
- Skip advanced topics, edge cases, troubleshooting
- **Beginner**: 2-3 foundational concepts maximum
- **Intermediate**: 4-5 core techniques
- **Advanced**: 3-4 specialized optimizations

### For MEDIUM courses (5-15 hours):
- Cover **core concepts + key applications**
- Include guided practice
- Some hands-on exercises
- Basic troubleshooting
- "Understand and apply fundamentals"
- **Beginner**: Build complete foundation, cover fundamentals thoroughly
- **Intermediate**: Focus 60% on application, 40% on concepts
- **Advanced**: Dive into architecture and design decisions

### For LONG courses (15-40 hours):
- **Comprehensive coverage**
- Extensive practice exercises
- Deep troubleshooting
- Multiple real-world applications
- Advanced techniques
- "Master the subject with confidence"
- **Beginner**: Complete journey from zero to competent practitioner
- **Intermediate**: From practitioner to advanced user
- **Advanced**: From advanced to expert-level mastery

### For EXTENSIVE courses (40+ hours):
- **Complete mastery**
- Edge cases and advanced patterns
- Multiple complex projects
- Performance optimization
- Integration with other topics
- "Expert-level understanding"
- **Beginner**: Zero to expert (rare but comprehensive)
- **Intermediate**: Expert-level depth in all areas
- **Advanced**: Thought leadership level, cutting-edge techniques

---

## Output Format (STRICT STRUCTURE)

### Course Header
```
# [TOPIC] - LLM-Only Course
**Duration**: [TIME_HOURS] hours
**Difficulty**: [BEGINNER/INTERMEDIATE/ADVANCED]
**Total Phases**: [X]
**Total Questions**: [Y]
**Completion Time**: [TIME_HOURS] hours ([Z] questions × [avg] min each)
```

### Learning Objectives
*After [TIME_HOURS] hours of LLM conversations, you will be able to:*
- [Objective 1 - realistic for time given]
- [Objective 2]
- [Objective 3]
- [List 3-5 objectives scaled to available time]

### Phase Structure
For each phase, use this EXACT format:

```
## Phase [N]: [Phase Name] ⏱️ [X.X hours]
**Level-Appropriate Focus**: [How this phase adapts to BEGINNER/INTERMEDIATE/ADVANCED]

**What you'll learn**: [2-3 sentence overview scaled to starting level]

### Questions:

1. **[Question Title]** ⏱️ [XX min] [Complexity: Simple/Standard/Deep/Complex]
   
   *Ask the LLM:*
   "Complete, copy-paste ready question that will generate a comprehensive response from the LLM..."
   
   *What you'll gain:*
   - [Specific skill/knowledge 1]
   - [Specific skill/knowledge 2]
   
   *Time factors:* Base [X]min + [reason for adjustment]

2. **[Question Title]** ⏱️ [XX min] [Complexity: Simple/Standard/Deep/Complex]
   
   *Ask the LLM:*
   "Next question..."
   
   *What you'll gain:*
   - [Specific outcome]
   
   *Time factors:* Base [X]min + [reason for adjustment]

[Continue for all questions in phase]

**Phase Completion Check** ⏱️ [5-10 min]:
- [Level-appropriate self-assessment question to ask the LLM]
```

### Time Distribution Summary
```
- Foundation: [X]h ([Y]%)
- Practice: [X]h ([Y]%)
- Application: [X]h ([Y]%)
- Review: [X]h ([Y]%)
```

### Study Schedule Suggestion
```
- Session 1 (Hour 1-2): Phases 1-2
- Session 2 (Hour 3-5): Phases 3-4
[Scale based on total hours]
```

---

## Automatic Scaling Rules (INTERNAL LOGIC)

When generating the course:

1. **Calculate total minutes available**: [TIME_HOURS] × 60

2. **Apply starting level time adjustment**:
   - Beginner: Total minutes × 0.83 (20% slower)
   - Intermediate: Total minutes × 1.0 (baseline)
   - Advanced: Total minutes × 1.1 (10% faster)

3. **Reserve buffer time**: Adjusted minutes × 0.85 (15% buffer)

4. **Determine average question time based on level and course length**:
   - Beginner + Short course: 12 min/question
   - Beginner + Medium course: 15 min/question
   - Beginner + Long course: 18 min/question
   - Intermediate + Short course: 10 min/question
   - Intermediate + Medium course: 13 min/question
   - Intermediate + Long course: 15 min/question
   - Advanced + Short course: 8 min/question
   - Advanced + Medium course: 11 min/question
   - Advanced + Long course: 13 min/question

5. **Calculate total questions**: Available minutes ÷ average question time

6. **Distribute questions into phases**: 3-6 questions per phase based on course length

7. **Assign complexity tags to each question**:
   - Simple (0.8x multiplier): Definitions, basic explanations
   - Standard (1.0x multiplier): Examples, guided walkthroughs
   - Deep (1.5x multiplier): Practice exercises, troubleshooting
   - Complex (2.0x multiplier): Multi-part problems, integration tasks

8. **Calculate individual question times**:
   - Start with average question time
   - Apply complexity multiplier
   - Document time factors for transparency

### Content Priority (when time is limited):

**Beginner Priority:**
1. Foundational definitions (must include - 30%)
2. Core concepts with simple examples (must include - 30%)
3. Basic applications (include if time permits - 20%)
4. Common mistakes (include if 10+ hours - 10%)
5. Intermediate techniques (include only if 20+ hours - 10%)

**Intermediate Priority:**
1. Core implementation techniques (must include - 25%)
2. Best practices and patterns (must include - 25%)
3. Real-world applications (must include - 25%)
4. Troubleshooting (include if time permits - 15%)
5. Advanced optimization (include only if 20+ hours - 10%)

**Advanced Priority:**
1. Complex architectures (must include - 20%)
2. Performance optimization (must include - 20%)
3. Edge cases and gotchas (must include - 20%)
4. Design trade-offs (must include - 20%)
5. Cutting-edge techniques (include if time permits - 20%)

### Verification Frequency (scales with time and level):

**Beginner:**
- <5 hours: Brief check after each phase
- 5-10 hours: Verification every 2 phases + final quiz
- 10-20 hours: Verification every phase + mid-course + final assessment
- 20+ hours: Regular checks + cumulative reviews every 5 phases

**Intermediate:**
- <5 hours: 1 verification at end
- 5-10 hours: Verification every 2-3 phases
- 10-20 hours: Verification every 3 phases + final
- 20+ hours: Self-directed checks + milestone assessments

**Advanced:**
- <5 hours: Self-assessment prompts only
- 5-10 hours: Verification at mid-point and end
- 10-20 hours: Challenge problems every 4-5 phases
- 20+ hours: Project-based validation + deep-dive assessments

---

## Quality Checklist

- [ ] Total estimated time matches [TIME_HOURS] input exactly
- [ ] Starting level ([BEGINNER/INTERMEDIATE/ADVANCED]) is reflected in:
  - [ ] Phase naming and descriptions
  - [ ] Question complexity and phrasing
  - [ ] Assumed prior knowledge
  - [ ] Depth of explanations requested
  - [ ] Time allocations (beginner gets more time)
- [ ] Each question includes complexity tag (Simple/Standard/Deep/Complex)
- [ ] Time estimates include documented adjustment factors
- [ ] Individual question times account for:
  - [ ] Expected response length
  - [ ] Complexity multiplier
  - [ ] Starting level adjustment
  - [ ] Practice/verification components
- [ ] Buffer time (15-20%) is included in calculations
- [ ] Each question is copy-paste ready
- [ ] No external dependencies required
- [ ] Progressive difficulty appropriate for level and time available
- [ ] Depth of coverage matches time constraint
- [ ] All questions generate complete, actionable LLM responses
- [ ] Total questions = (TIME_HOURS × 60 × level_multiplier × 0.85) ÷ avg_min_per_question
- [ ] Verification frequency matches both time available and starting level
- [ ] Content priorities align with level (beginner = more foundation, advanced = more optimization)

---

## Example Usage

**Input:**
- Topic: Critical Thinking
- Time: 3 hours
- Level: Beginner

**Output:** 
- 2-3 phases, 10-12 questions
- Focus on essential concepts only
- +20% time for beginner processing
- Simple complexity tags, heavy on definitions
- Questions like "Explain what critical thinking is with everyday examples..."

**Input:**
- Topic: Critical Thinking
- Time: 3 hours
- Level: Advanced

**Output:**
- 3-4 phases, 14-16 questions (10% more efficient)
- Skip definitions, focus on application
- Deep complexity tags, heavy on analysis
- Questions like "Compare systematic vs heuristic approaches in high-stakes decision-making..."

**Input:**
- Topic: Docker
- Time: 24 hours  
- Level: Beginner

**Output:** 
- 15-18 phases, 70-80 questions
- Comprehensive coverage from zero knowledge
- Mix of Simple/Standard/Deep complexity
- Strong emphasis on fundamentals (first 30% of course)
- Questions like "Explain what containerization is and why it matters, using simple analogies..."

**Input:**
- Topic: Docker
- Time: 24 hours
- Level: Advanced

**Output:**
- 15-18 phases, 90-100 questions (more efficient, more content)
- Skip basics, jump to orchestration and optimization
- Heavy on Deep/Complex tags
- Questions like "Analyze the trade-offs between Docker Swarm and Kubernetes for production deployments..."

---

## NOW GENERATE:

**Topic**: [INSERT TOPIC HERE]
**Available Time**: [INSERT HOURS] hours
**Starting Level**: [BEGINNER/INTERMEDIATE/ADVANCED]

Create the complete time-optimized LLM-only course outline following the structure above.
