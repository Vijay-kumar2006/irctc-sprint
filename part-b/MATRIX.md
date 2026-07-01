# Impact vs Effort Matrix

## The Matrix

|                   | Low Effort | High Effort |
|-------------------|------------|-------------|
| **High Impact** | Persistent Search Filters, Smart PNR Status Dashboard | Virtual Tatkal Queue System, Reliable Seat Selection |
| **Low Impact** | Mobile-Friendly Homepage | Real-Time Payment Status Tracker |

---

# How I Scored Each Dimension

## Impact Scoring (1–5)

Impact was measured based on:

- Number of users affected
- Importance in the booking journey
- Effect on successful ticket booking
- Customer satisfaction

## Effort Scoring (1–5)

Effort was measured based on:

- Backend development complexity
- Frontend UI changes
- Database modifications
- API dependencies
- Infrastructure requirements

---

# Placement Justifications

## 1. Virtual Tatkal Queue System – High Impact / High Effort

**Impact:**  
Millions of users attempt Tatkal booking every day. Solving server crashes significantly improves the booking experience.

**Effort:**  
Requires introducing a queue management system, WebSockets, Redis, and changes to booking services.

**Priority:**  
Highest priority because it solves the biggest issue affecting the largest number of users.

---

## 2. Persistent Search Filters – High Impact / Low Effort

**Impact:**  
Nearly every user searches for trains and uses filters. Retaining filter selections saves time and reduces frustration.

**Effort:**  
Requires only frontend state management and minor backend support.

**Priority:**  
Quick win with noticeable user experience improvements.

---

## 3. Reliable Seat Selection – High Impact / High Effort

**Impact:**  
Families, senior citizens, and users with berth preferences benefit directly.

**Effort:**  
Needs updates to seat allocation, reservation logic, and synchronization across services.

**Priority:**  
Should be implemented after the Tatkal queue system.

---

## 4. Real-Time Payment Status Tracker – Low Impact / Low-Medium Effort

**Impact:**  
Improves user confidence during payment and reduces duplicate transactions.

**Effort:**  
Requires integration with payment gateways and status polling.

**Priority:**  
Useful enhancement after core booking issues are addressed.

---

## 5. Smart PNR Status Dashboard – High Impact / Low Effort

**Impact:**  
Helps users understand booking status without external resources.

**Effort:**  
Primarily a frontend redesign using existing Railway API data.

**Priority:**  
Easy to build and provides significant usability improvements.

---

## 6. Mobile-Friendly Homepage – Low Impact / Low Effort

**Impact:**  
Improves navigation for mobile users but does not directly affect booking success.

**Effort:**  
Mostly responsive UI improvements with minimal backend work.

**Priority:**  
Can be completed alongside other UI improvements.

---

# Recommended Sprint Order

1. Virtual Tatkal Queue System
2. Persistent Search Filters
3. Reliable Seat Selection
4. Smart PNR Status Dashboard
5. Real-Time Payment Status Tracker
6. Mobile-Friendly Homepage