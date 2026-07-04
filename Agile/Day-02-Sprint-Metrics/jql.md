# Useful JQL

## Current Sprint

Sprint in openSprints()

---

## Current Sprint Done

Sprint in openSprints()
AND statusCategory = Done

---

## Current Sprint Not Done

Sprint in openSprints()
AND statusCategory != Done

---

## Added During Sprint

issuekey in addedAfterSprintStart()

> نیازمند ScriptRunner یا افزونه مشابه

---

## High Priority in Sprint

Sprint in openSprints()
AND priority in (Highest, High)

---

## Current Sprint Bugs

Sprint in openSprints()
AND issuetype = Bug
