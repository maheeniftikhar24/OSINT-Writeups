# TryHackMe: Missing Person Walkthrough

![Platform](https://img.shields.io/badge/Platform-TryHackMe-red)
![Category](https://img.shields.io/badge/Category-OSINT-blue)
![Difficulty](https://img.shields.io/badge/Difficulty-Easy-green)

![TryHackMe Missing Person Room](Missing%20Person%20room.jpeg)

> **Room:** [TryHackMe – Missing Person](https://tryhackme.com/room/missingperson)
> **Platform:** TryHackMe
> **Difficulty:** Easy
> **Category:** OSINT (Open Source Intelligence)

## Disclaimer

This write-up is intended for educational purposes. It focuses on the **OSINT methodology and reasoning** used to solve the challenge rather than simply listing answers.

> 📄 **Detailed Walkthrough:** [View the full PDF walkthrough](./Missing-Person-Walkthrough.pdf)

## Table of Contents

* [Introduction](#introduction)
* [Scenario](#scenario)
* [Tools Used](#tools-used)
* [Investigation](#investigation)
* [Key Takeaways](#key-takeaways)
* [Final Answers](#final-answers)
* [GitHub Support](#github-support)
* [Conclusion](#conclusion)

## Introduction

This write-up covers my investigation of the **Missing Person** room on TryHackMe.

The challenge uses OSINT techniques to identify locations, people, and other clues from publicly available information. I’ll briefly explain the **approach, tools, and reasoning** used to follow each clue rather than simply listing the answers.

## Scenario

![TryHackMe Missing Person Scenario](Scenario.png)

> **Task 1 – OSINT**
>
> *"My friend went on holiday in 2025 and shared some photos, but I haven't heard from him since. Can you help me track him down for the police report?"*

The task provides a downloadable ZIP file containing the materials needed to begin the investigation.


## Tools Used

* **ExifTool** – Extract image metadata
* **Google Search** – Research locations, events, and people
* **Google Maps** – Verify locations and addresses
* **Social Media** – Follow public profiles and clues
* **TryHackMe** – Challenge environment

## Investigation

### 1. Identify the MotoGP Circuit

The first clue was the MotoGP photo.

I searched for MotoGP events in Indonesia during 2025 and identified the circuit as:

**Pertamina Mandalika International Street Circuit**

The event took place from:

**03-05/10/2025**

This established the approximate location and timeframe for the investigation.

### 2. Check the Image Metadata

The provided images contained useful metadata.

Using ExifTool on `food.jpg`, I found:

```text
DateTimeOriginal: 2025:10:05 19:55:30
```

Therefore, the photo was taken at:

**19:55:30**

This demonstrated how image metadata can provide valuable clues without needing to visually identify everything in the image.

### 3. Identify the Restaurant

The food photo contained visible branding on the table cover.

Searching the name led to:

**Cantina Mexicana**

The restaurant is located in **Kuta, Lombok**, matching the investigation's location.

### 4. Find the After-Party Location

The next clue mentioned a MotoGP after-party.

Using the restaurant/location information and searches for local MotoGP events and nightlife, I identified the relevant bar location.

The address found was:

**Jl. Raya Kuta, Kuta, Kec. Pujut, Kabupaten Lombok Tengah, Nusa Tenggara Barat**

### 5. Identify the DJ

The investigation then focused on the local DJ mentioned in the message.

Searching the after-party information and related social media profiles led to the DJ's stage name:

**Bong Leleh**

His Instagram username was:

**@bongleleh**

This provided another pivot point for the investigation.

### 6. Follow the DJ's Online Accounts

Instead of stopping at the Instagram profile, I checked the DJ's other publicly available online information.

This revealed that he also operates a **tour business**, which provided another clue connected to the missing person's message about visiting a cave.

Following this information led to the cave location:

**Gua Sumur**

### 7. Find the Tour Business Number

The final clue was the phone number listed for the DJ's tour business.

The number was:

**085333137345**

## Key Takeaways

* Always inspect **image metadata** when investigating photos.
* Use one confirmed clue to search for the **next clue**.
* Cross-check information across multiple sources.
* Social media can reveal useful connections between people, places, and businesses.
* Avoid relying on a single search result; **verify important findings**.

## Final Answers

| # | Answer                                                                        |
| - | ----------------------------------------------------------------------------- |
| 1 | Pertamina Mandalika International Street Circuit                              |
| 2 | 03-05/10/2025                                                                 |
| 3 | Cantina Mexicana                                                              |
| 4 | 19:55:30                                                                      |
| 5 | Jl. Raya Kuta, Kuta, Kec. Pujut, Kabupaten Lombok Tengah, Nusa Tenggara Barat |
| 6 | Bong Leleh                                                                    |
| 7 | Gua Sumur                                                                     |
| 8 | 085333137345                                                                  |

## GitHub Support

If you found this write-up useful, consider giving the repository a **⭐ Star** on GitHub.

It helps support my cybersecurity and OSINT learning journey and encourages me to continue documenting more investigations and write-ups.

**Found an issue or have a suggestion?** Feel free to open an issue or share your feedback.

## Conclusion

The **Missing Person** room demonstrates how a simple photo can lead to a larger OSINT investigation.

The key lesson is to treat every piece of information as a potential **pivot point** and gradually connect clues until the full picture becomes clear.
