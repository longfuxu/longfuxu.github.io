---
layout: post
title: "Lab Notes: Troubleshooting Optical Tweezers Drift"
date: 2024-07-15
description: Technical notes on solving drift issues in force spectroscopy experiments
tags: [lab-notes, optical-tweezers, troubleshooting]
categories: [methods]
robots: noindex
---

**Problem:** Seeing systematic drift in force measurements over 30+ minute experiments. Force baseline shifts by ~0.5 pN/hour.

## Investigation Steps

### 1. Temperature Stability
- **Check:** Room temperature variation
- **Result:** ±0.2°C variation over experiment duration
- **Action:** Increased lab climate control, added thermal insulation around optics table

### 2. Laser Power Stability
- **Check:** 1064 nm laser output over time
- **Result:** <0.1% variation (within spec)
- **Conclusion:** Not the primary cause

### 3. Sample Chamber Issues
- **Check:** Evaporation from sample wells
- **Result:** Significant volume loss over 30 min
- **Action:** Switched to sealed flow cells, added humidification chamber

### 4. Optical Alignment
- **Check:** QPD alignment stability
- **Result:** Minor drift in X/Y positioning
- **Action:** Improved mounting, added reference measurements

## Solution

Primary cause was sample evaporation leading to:
- Changed refractive index near coverslip
- Altered optical path length
- Systematic force calibration drift

**Fix:** Custom flow cell design with:
- Minimal dead volume
- Continuous perfusion capability  
- Temperature control via Peltier elements

## Results
- Drift reduced to <0.1 pN/hour
- Experiment duration extended to 2+ hours
- More reliable long-term measurements

## Notes for Next Time
- Always check environmental stability first
- Document baseline conditions at start/end
- Include reference measurements in experimental design

**Related:** [Force Calibration Protocols](/blog/2024/force-calibration/), [Single-Molecule Setup Guide](/blog/2024/sm-setup/)

---

*These technical notes are primarily for lab reference but may be useful for others working with similar equipment.*