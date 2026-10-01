# Project 2 — Evidence

This document contains evidence for the six required project tests per the Project Rubric.

## Test 1 — Order Tracking

Prompt:
> What is the current status of order ORD-001? Include the carrier,
> tracking number, and estimated delivery date if available.

![Order Tracking](./test-evidence-1-order-tracking.png)

---

## Test 2 — Refund Processing

Prompt:
> Please process a refund for order ORD-002 and tell me the result.

![Refund Processing](./test-evidence-2-refund-processing.png)

---

## Test 3 — Knowledge Base / RAG

Prompt:
> What is the warranty policy for devices? Please answer using the
> support knowledge base.

![Knowledge Base](./test-evidence-3-knowledge-base.png)

---

## Test 4 — Long-Term Memory

Session 1:
> Please remember that I prefer device recommendations under $300.

![Memory Session 1](./test-evidence-4-memory-session-1.png)

Session 2:
> What kind of product recommendations do I prefer?

![Memory Session 2](./test-evidence-4-memory-session-2.png)

The two prompts were run under different session IDs using the same customer ID.

---

## Test 5 — Loyalty Discount

Prompt:
> Calculate my loyalty discount. I have 4250 points, I am Gold tier,
> my order total is $200, and the product category is device.
> Show the full breakdown.

![Loyalty Discount](./test-evidence-5-loyalty-discount.png)

---

## Test 6 — Browser Tool

Prompt:
> Use the browser to visit the AWS Bedrock AgentCore documentation
> and tell me the page title and briefly summarize what AgentCore is.

![Browser Tool](./test-evidence-6-browser.png)

---

## CloudWatch Alarm

A CloudWatch metric filter and alarm were configured for the AgentCore runtime logs.

- Metric namespace: `AgentCoreProject`
- Metric: `AgentRuntimeErrors`
- Threshold: `>= 1`
- Period: `5 minutes`
- Datapoints to alarm: `1 out of 1`

The alarm is designed to flag runtime `ERROR` log events.

![CloudWatch Alarm](./cloudwatch-alarm.png)