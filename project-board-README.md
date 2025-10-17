
---

# BABS Project Research Board

## Overview

This project covers the Fall 2025 efforts to perform precedent research and develop a design for the deployment of a proof of concept Biological system in which computational intelligence can become aware of the biological state of physical cognitive agents within the blended environment. The goal of this project stage will be to investigate the translation of biosensory input from cognitive agents (human) to audiovisual output.


## Board Structure

### 5-Column Kanban Workflow

| Column | Purpose | Description |
|--------|---------|-------------|
| 📋 **Backlog** | Ready Tasks | Refined issues ready for assignment |
| 👤 **Assigned** | Committed Work | Tasks assigned and ready to start |
| ⚡ **Active** | In Progress | Currently active work (limit 2-3 items) |
| 🔵 **Review** | Quality Control | Work ready for faculty/peer review |
| ✅ **Done** | Completed | Finished and assessed work |

## SRDMPA Methodology Integration

Research phases are tracked through **issue labels**, not board columns:

- `01-speculate` - Research questions, hypotheses, initial ideas
- `02-research` - Literature review, data collection, investigation  
- `03-design` - Planning experiments, designing methods, prototyping
- `04-make` - Implementation, coding, data analysis, creation
- `05-publish` - Documentation, writing, presentation preparation
- `06-assess` - Evaluation, reflection, iteration planning

## Workflow Examples

### Individual Research Project
```
Speculation → Create Issue → Backlog → Assign to Self → Research → Active → Review → Assess → Done
```

### Team Research Project  
```
Team Meeting → Prioritize Backlog → Faculty Assigns → Student Works → Submit for Review → Complete
```

## Getting Started

### 1. Create Your Research Issues

Use the **CHI Issue Templates**:
- **Milestone** - Define concrete deliverables and acceptance criteria
- **Research Log** - Weekly notes, sources, and phase tracking
- **AI Collaboration Report** - Document AI tool usage and contributions
- **Bug Report** - Technical issues and debugging tasks

### 2. Apply SRDMPA Labels

Tag each issue with the appropriate research phase:
```markdown
- Milestone: "Complete literature review analysis" → 01-speculate + 02-research
- Research Log: "Week 23-15 AI bias investigation" → 02-research  
- Milestone: "Build bias detection prototype" → 03-design + 04-make
- Research Log: "Week 23-16 Statistical analysis" → 04-make
- Milestone: "Draft conference paper" → 05-publish
- Research Log: "Week 23-17 Reflection on methods" → 06-assess
```

### 3. Move Issues Through Columns

**Backlog → Assigned:**
- During weekly planning meetings
- When committing to work for the sprint/week
- Self-assignment for individual projects

**Assigned → Active:**  
- When actually starting the work
- Limit to 2-3 active items to maintain focus

**Active → Review:**
- When work is complete and needs feedback
- Research methodology validation required
- Documentation/code review needed

**Review → Done:**
- After faculty/peer approval
- Quality standards met
- Ready to build upon for next phase

## Best Practices

### For Students
- **Start with speculation** - Create issues with `01-speculate` for all research ideas
- **Limit active work** - Keep 2-3 items in Active column maximum  
- **Seek review actively** - Move work to Review column when ready for feedback
- **Update labels** - Add new SRDMPA phase labels as work evolves
- **Weekly planning** - Review and assign upcoming work during meetings

### For Faculty Advisors
- **Monitor master board** - Use CHI-StudentResearch project board for oversight across all students
- **Link student projects** - Connect individual student boards to master tracking system
- **Review backlog priorities** - Help students focus on high-impact work during weekly meetings
- **Provide timely feedback** - Monitor Review column for work needing attention
- **Track methodology** - Ensure SRDMPA phases are properly represented across projects
- **Celebrate completion** - Acknowledge work moving to Done column and major milestone achievements

### For Research Teams
- **Collaborative planning** - Use weekly meetings to assign from backlog
- **Clear ownership** - One person per assigned issue
- **Cross-review** - Team members can review each other's work
- **Knowledge sharing** - Comment on issues to share insights

### **Milestones:**
1. **Title:** `Milestone:  Sensor Setup and Calibration`
   - **Phase:** `01-research`
   - **Goal:** Identification and Calibration of Sensors
   - **Criteria:** 
     - [ ] Identifying which biosensors (consumer, research, primitive, or camera-based) will be trialed for the MVP
     - [ ] Unboxing, testing, and calibrating sensors
     - [ ] Ensuring at least one source can reliably produce usable data streams
   - **Due:** 2025-10-10

2. **Title:** `Milestone: Pipeline Integration`
   - **Phase:** `02-make`  
   - **Goal:** Software to sensor mediation pathway establishment
   - **Criteria:**
     - [ ] Establishing the mediation pathway from sensor to software using LSL, OSC, or BLE
     - [ ] Seeing live data flow in a normalized format, ready for mapping
  - **Due:** 2025-10-24

3. **Title:** `Milestone: MAX/MSP Patch Development`
   - **Phase:** `03  
   - **Goal:** Biosignal to Audiovisual Translation
   - **Criteria:** 
     - [ ] Translating raw biosignal data into audiovisual events using Max/MSP and Jitter
     - [ ] Responsiveness, even if the mapping is simple or rough
 - **Due:** 2025-11-07
    
4. **Title:** `Milestone: Projection Sandbox Demo`
   - **Phase:** `04  
   - **Goal:** Installation and demonstration of single-surface projection environment
   - **Criteria:** 
     - [ ] Installing the single-surface projection environment
     - [ ] Visible demonstration of a bio-aware blended mediation pathway
     - [ ] Linking sensor → data → audiovisual projection
 - **Due:** 2025-11-21
    
5. **Title:** `Milestone: Refinement`
   - **Phase:** `05 
   - **Goal:** Pipeline refinement for stability and reliability
   - **Criteria:** 
     - [ ] Focuses on improving the stability, latency, and reliability of the pipeline
     - [ ] Visible demonstration of a bio-aware blended mediation pathway
     - [ ] Consolidates the prototype into a smoother, more predictable demo system
 - **Due:** 2025-11-28

6. **Title:** `Milestone: Documentation & Showcase`
   - **Phase:** `06 
   - **Goal:** Documentation of mediation pathways and MVP Showcase
   - **Criteria:** 
     - [ ] Produces written guides, troubleshooting notes, and diagrams of mediation pathways
     - [ ] Culminates in a final MVP showcase that demonstrates successful bio → environment transformation
 - **Due:** 2025-12-05
    
## Integration with CHI Research Ecosystem

This individual project board integrates with the broader CHI research management system:

### **CHI Research Architecture:**
- **Master Project Board** - Located in `CHI-StudentResearch` repository for faculty oversight
- **Individual Project Boards** - This template creates detailed workflow boards for each student
- **Repository Templates** - `CHI-Research-Template` provides standardized project structure

### **Two-Tier Project Management:**

**Faculty Level (Master Board in CHI-StudentResearch):**
- High-level tracking of all student research projects
- Links to individual student project boards for detailed monitoring
- Cross-project coordination and resource allocation
- Milestone tracking and deadline management

**Student Level (Individual Project Board - This Template):**
- Daily and weekly task management using SRDMPA methodology
- Detailed workflow: Backlog → Assigned → Active → Review → Done
- Research phase tracking through issue labels
- Personal productivity and research progress

### **Integration Workflow:**
1. **Student creates repository** from CHI-Research-Template
2. **Student creates project board** using this template
3. **Faculty links student project** to master board in CHI-StudentResearch
4. **Regular reporting** flows from individual to master board level

This project board works seamlessly with:
- **CHI Issue Templates** - Structured issue creation
- **SRDMPA Labels** - Automated via repository template
- **GitHub Actions** - Automated project setup and linking
- **Documentation Standards** - Issue tracking supports reproducible research

## Troubleshooting

**Common Issues:**

**"Too many columns don't fit on screen"**
- Use browser zoom out (Ctrl/Cmd + -)
- Focus on 2-3 relevant columns at a time
- Use GitHub's column collapse feature

**"Issues stuck in Review"** 
- Set review SLAs (e.g., 48 hours for feedback)
- Use `needs-review` label to highlight urgency
- Schedule regular review sessions

**"Backlog becomes overwhelming"**
- Regular backlog grooming sessions
- Archive or close outdated issues  
- Focus on current research priorities

**"Individual projects don't need Assigned column"**
- Use it for personal commitment ("This week I will...")
- Self-assignment creates accountability
- Can skip directly to Active if preferred

## Support

For questions about this project board template:
- Review CHI Research Template documentation
- Contact CHI faculty advisors
- Reference GitHub Projects documentation
- Check CHI methodology resources

---
