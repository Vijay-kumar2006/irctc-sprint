# IRCTC Problem Discovery — Part A

## Summary

- Total Problems: 6
- Platform: irctc.co.in
- Device: Desktop Chrome

## Problem 1: Tatkal Booking Crashes at 10:00 AM (Given)

### What is broken
The IRCTC server becomes unresponsive when Tatkal booking opens at 10 AM. Users experience loading screens, server errors, and session timeouts.

### Affected users
Millions of users trying to book Tatkal tickets.

### Frequency
Occurs daily around 10:00 AM.

### Current Flow

1. User logs into IRCTC.
2. Searches for a train.
3. Selects Tatkal quota.
4. Fills passenger details.
5. Clicks Book Now at 10 AM.
6. Page freezes or shows HTTP 502.
7. User refreshes and loses the ticket.

### Where exactly it breaks

The failure occurs after clicking **Book Now** because the servers receive extremely high traffic.

## Problem 2: Search Filters Do Not Work Reliably (Given)

### What is broken
Search filters sometimes display incorrect trains or reset automatically.

### Affected users
All users searching for trains.

### Frequency
Frequently during peak hours.

### Current Flow

1. User searches trains.
2. Results appear.
3. User selects Sleeper and Available filters.
4. Results reload.
5. Waitlisted trains still appear.
6. User goes back.
7. Filters reset.

### Where exactly it breaks

The filter state is lost after refreshing search results.

## Problem 3: Seat Selection Resets (Given)

### What is broken
Selected seats are replaced by automatic allocation.

### Affected users
Families and elderly passengers.

### Frequency
Around 15–25% of booking sessions.

### Current Flow

1. User selects train.
2. Opens seat map.
3. Selects lower berth.
4. Clicks Proceed.
5. Passenger page shows Auto.
6. User returns.
7. Selected seat is unavailable.

### Where exactly it breaks

The selected seat information is not carried to the next page.

## Problem 4: No Payment Progress Indicator (Self-Discovered)

### What is broken
Users do not know whether payment is processing or has failed.

### How I found it
I proceeded to the payment page and selected UPI.

### Screenshot/Description
The payment page only displays a loading spinner. There is no progress bar or payment status message.

### Affected users
UPI and Net Banking users.

### Frequency
Occasionally during heavy traffic.

### Current Flow

1. Search train.
2. Select passengers.
3. Click Continue.
4. Choose UPI.
5. Click Pay.
6. Loading spinner appears.
7. User waits without feedback.

### Where exactly it breaks

The payment processing page lacks real-time status updates.

## Problem 5: Confusing PNR Status Page (Self-Discovered)

### What is broken
The PNR page does not explain booking statuses clearly.

### How I found it
I opened the PNR Status page.

### Screenshot/Description
The page displays technical terms such as WL, RAC, and CNF without explaining them.

### Affected users
New users and elderly passengers.

### Frequency
Always.

### Current Flow

1. Open PNR Status.
2. Enter PNR number.
3. Click Submit.
4. Booking status appears.
5. Technical abbreviations are displayed.
6. User cannot understand them.
7. User searches elsewhere.

### Where exactly it breaks

The page provides no explanation for booking status abbreviations.

## Problem 6: Mobile Website Navigation is Difficult (Self-Discovered)

### What is broken
The mobile layout is crowded and difficult to navigate.

### How I found it
I opened the website in Chrome on my phone.

### Screenshot/Description
Important options require excessive scrolling, and buttons are small.

### Affected users
Mobile users.

### Frequency
Always.

### Current Flow

1. Open website.
2. Homepage loads.
3. Scroll to find Train Search.
4. Open booking page.
5. Try navigating.
6. Buttons are difficult to tap.
7. User experiences frustration.

### Where exactly it breaks

The homepage is not optimized for smaller screens.

