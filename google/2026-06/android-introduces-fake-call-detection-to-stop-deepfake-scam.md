---
title: "Android introduces fake call detection to stop deepfake scams"
vendor: google
source_url: https://blog.google/security/android-fake-call-detection/
published_at: 2026-06-02T18:00:00.000Z
crawled_at: 2026-06-09T02:01:23.385Z
word_count: 1301
reading_time_minutes: 7
tags: [gpt, gemini, multimodal, agents, api, product]
---

[Android Security](https://blog.google/security/android-security/)

# How Android helps keep you safe from impersonation scams with fake call detection

Jun 02, 2026

·

4 min read

Share

[x.com](https://twitter.com/intent/tweet?text=How%20Android%20helps%20keep%20you%20safe%20from%20impersonation%20scams%20with%20fake%20call%20detection%20%40google&url=https://blog.google/security/android-fake-call-detection/) [Facebook](https://www.facebook.com/sharer/sharer.php?caption=How%20Android%20helps%20keep%20you%20safe%20from%20impersonation%20scams%20with%20fake%20call%20detection&u=https://blog.google/security/android-fake-call-detection/) [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/security/android-fake-call-detection/&title=How%20Android%20helps%20keep%20you%20safe%20from%20impersonation%20scams%20with%20fake%20call%20detection) [Mail](mailto:?subject=How%20Android%20helps%20keep%20you%20safe%20from%20impersonation%20scams%20with%20fake%20call%20detection&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0AHow%20Android%20helps%20keep%20you%20safe%20from%20impersonation%20scams%20with%20fake%20call%20detection%0A%0AFake%20call%20detection%20on%20Android%20helps%20protect%20you%20from%20scammers%20using%20AI%20deepfakes%20to%20impersonate%20your%20contacts.%0A%0Ahttps://blog.google/security/android-fake-call-detection/)

Copy link

Fake call detection on Android helps protect you from scammers using AI deepfakes to impersonate your contacts.


E

Eric Lynch

Product Manager


T

Troy Kensinger

Technical Program Manager


O

Oren Schetrit

Senior Product Manager


Share

[x.com](https://twitter.com/intent/tweet?text=How%20Android%20helps%20keep%20you%20safe%20from%20impersonation%20scams%20with%20fake%20call%20detection%20%40google&url=https://blog.google/security/android-fake-call-detection/) [Facebook](https://www.facebook.com/sharer/sharer.php?caption=How%20Android%20helps%20keep%20you%20safe%20from%20impersonation%20scams%20with%20fake%20call%20detection&u=https://blog.google/security/android-fake-call-detection/) [LinkedIn](https://www.linkedin.com/shareArticle?mini=true&url=https://blog.google/security/android-fake-call-detection/&title=How%20Android%20helps%20keep%20you%20safe%20from%20impersonation%20scams%20with%20fake%20call%20detection) [Mail](mailto:?subject=How%20Android%20helps%20keep%20you%20safe%20from%20impersonation%20scams%20with%20fake%20call%20detection&body=Check%20out%20this%20article%20on%20the%20Keyword:%0A%0AHow%20Android%20helps%20keep%20you%20safe%20from%20impersonation%20scams%20with%20fake%20call%20detection%0A%0AFake%20call%20detection%20on%20Android%20helps%20protect%20you%20from%20scammers%20using%20AI%20deepfakes%20to%20impersonate%20your%20contacts.%0A%0Ahttps://blog.google/security/android-fake-call-detection/)

Copy link



Imagine your phone rings. The caller ID says "Mom." You answer, and it sounds exactly like her; she has the same tone, the same voice. However, the person on the other end isn't your mom — it’s a scammer using AI tools to impersonate her and demand money from you for a fake emergency.

To help protect you from the growing threat of impersonation scams, Android is introducing fake call detection, an industry-first protection that can detect and flag suspected spoofed calls when your contact and you are both using Phone by Google. This builds on our recent launch of [verified financial calls](https://blog.google/security/whats-new-in-android-security-privacy-2026/#:~:text=banking%20scam%20calls-,Scammers,-are%20impersonating%20financial), which warns you if a scammer is attempting to impersonate your financial institution.

Marking a major milestone in mobile security, fake call detection helps protect you, your family and friends by identifying when a caller isn’t who they claim to be, giving you an extra layer of defense against sophisticated AI-voice cloning scams, also called deepfake attacks, of your contacts.

### **The Growing Threat of Impersonation Attacks**

Phone and online scams are a massive and growing problem. INTERPOL’s [March 2026 Global Financial Fraud Threat Assessment](https://www.interpol.int/en/News-and-Events/News/2026/INTERPOL-report-warns-of-increasingly-sophisticated-global-financial-fraud-threat) cited impersonation fraud as one of the leading contributors to over $400 billion in global losses. Impersonation scams are also among the [top reported frauds to the FTC](https://www.ftc.gov/news-events/news/press-releases/2025/04/ftc-highlights-actions-protect-consumers-impersonation-scams), with losses totaling $2.95 billion in 2024 and growing worldwide. For years, people have relied on caller ID to know who is on the other end of the line, but this is no longer sufficient due to scammers’ new tactics.

With many people refusing to pick up calls from unknown numbers, scammers are shifting strategies and impersonating the phone numbers of contacts. Scammers are combining two powerful tactics to steal your money and data:

1. Scammers _spoof_ the phone number, routing calls through internet-based software to make it appear as though the call is originating from a familiar, contact.
2. Then they use easily accessible _AI deepfake technology_ to sound exactly like an authority figure, family member, or employer. In fact, [experts say](https://www.cnn.com/2026/05/29/tech/ai-voice-cloning-scams-protect-yourself) AI audio deepfakes have become so realistic that most people can no longer reliably distinguish them from real human voices.



### **How Android Detects and Alerts You of Fake Calls**

This feature is on by default and works automatically behind the scenes. Think of it like a digital handshake between devices. When a contact calls you and you’re both using Phone by Google, their device sends a silent confirmation signal in real time to your device to verify the call is legitimate and truly coming from the contact’s device. Because this digital handshake uses end-to-end encrypted Rich Communication Services (RCS) technology, it is completely private.

If a scammer tries to impersonate your contact, that initial confirmation signal will be missing. Your device will instantly notice this and ping your contact's actual device to double-check. If their real device says, "I'm not making a call right now," you'll get a warning on your screen advising you to hang up immediately. This proactive alert helps you avoid falling victim to deepfake impersonation and call spoofing in real time. You can disable this feature at any time in the [Phone by Google app settings](https://support.google.com/phoneapp/answer/3459196?hl=en).

Sorry, your browser doesn't support embedded videos, but don't worry, you can [download it](https://storage.googleapis.com/gweb-uniblog-publish-prod/original_videos/Fake_Call_Detection_Animation_2.mp4) and watch it with your favorite video player!

### **Availability**

We are rolling out fake call detection globally in Phone by Google to Android 12+ devices this month starting with Pixel devices

[1](https://blog.google/security/android-fake-call-detection/#footnote-1)
. Phone by Google is already the default phone app for the majority of Android devices. If your device uses a different app, you can [install Phone by Google](https://play.google.com/store/apps/details?id=com.google.android.dialer&hl=en_US) from the Play Store and set it as your default phone app to help protect yourself from fake calls.

Security shouldn’t be limited to just one type of phone or app. We want to raise the bar across the industry to help protect as many people as possible. That’s why we built this feature on top of [Rich Communication Services (RCS)](https://www.gsma.com/solutions-and-impact/technologies/networks/rcs/), an open standard – making it possible for other apps and device manufacturers to adopt this technology.

Spot scammers pretending to be trusted contacts with fake call detection - YouTube

Tap to unmute

[Spot scammers pretending to be trusted contacts with fake call detection](https://www.youtube.com/watch?v=IMkmrUqc7R0) [Android](https://www.youtube-nocookie.com/channel/UC9M7-jzdU8CVrQo1JwmIdWA)

Android1.26M subscribers

[Watch on](https://www.youtube.com/watch?v=IMkmrUqc7R0)



1:39

### **Google’s Continued Leadership in Protecting Users**

Google has a long history of leading the fight against impersonation and scams:

- AI-powered [Scam Detection in Google Messages automatically helps protect](https://blog.google/security/new-ai-powered-scam-detection-features/) Android users from malicious scam texts. And for extra peace of mind, Pixel and Samsung users can also enable [Scam Detection in the Phone by Google app to flag scam calls](https://blog.google/security/staying-one-step-ahead-strengthening-androids-lead-in-scam-protection/).
- In Gmail we support [Brand Indicators for Message Identification (BIMI)](https://workspaceupdates.googleblog.com/2024/09/gmail-additional-bimi-protections.html).
- With [RCS for Business](https://rcsforbusiness.google/), senders are verified so you know exactly which businesses are contacting you.
- We’ve championed and integrated [STIR/SHAKEN authentication](https://developer.android.com/develop/connectivity/telecom/dialer-app/prevent-spoofing) at the network level in multiple countries.

Fake call detection represents the next major step in our industry-leading protections against scams. As scammers grow more sophisticated, we are continuing to expand and evolve our protections.

POSTED IN:

Read more

* * *

More Information

* * *

[1](https://blog.google/security/android-fake-call-detection/#footnote-source-1 "Jump up")

_Available on Android 12+ devices with Phone by Google, Contacts, and Google Messages installed. Requires RCS capability in Google Messages. Both contact and call recipient must use Phone by Google._

Collapse

* * *

### Related stories

[\\
\\
Android Security **What’s New in Android Security and Privacy in 2026**\\
\\
By\\
\\
\\
\\
Eugene Liderman\\
\\
\\
May 12, 2026](https://blog.google/security/whats-new-in-android-security-privacy-2026/)

[\\
\\
Android Security **Android’s Agentic Future: Building Gemini Intelligence on a Foundation of Security & Privacy**\\
\\
By\\
\\
\\
\\
Dave Kleidermacher\\
\\
\\
May 12, 2026](https://blog.google/security/android-gemini-intelligence-security-privacy/)

[\\
\\
Android Security **Evolving Verifiable Trust: Bringing Binary Transparency to the Android Ecosystem**\\
\\
By\\
\\
\\
\\
Dave Kleidermacher\\
\\
\\
\\
&\\
\\
\\
Eric Lynch\\
\\
\\
\\
&\\
\\
\\
Billy Lau\\
\\
\\
\\
&\\
\\
\\
Vikram Gaur\\
\\
\\
\\
&\\
\\
\\
Kevin Chao\\
\\
\\
May 04, 2026](https://blog.google/security/bringing-binary-transparency-to-the-android-ecosystem/)

[Android Security **Bringing Rust to the Pixel Baseband** \\
\\
Google is continuously advancing the security of Pixel devices.\\
\\
By\\
\\
\\
\\
Jiacheng Lu\\
\\
\\
Apr 10, 2026](https://blog.google/security/bringing-rust-to-the-pixel-baseband/)

[Android Security **Security for the Quantum Era: Implementing Post-Quantum Cryptography in Android** \\
\\
Modern digital security is at a turning point. We are on the threshold of using quantum computers to solve "impossible" problems in drug discovery, materials science, an…\\
\\
By\\
\\
\\
\\
Eric Lynch\\
\\
\\
\\
&\\
\\
\\
Dom Elliott\\
\\
\\
Mar 25, 2026](https://blog.google/security/security-for-the-quantum-era-implementing-post-quantum-cryptography-in-android/)

[\\
\\
Android Security **Staying One Step Ahead: Strengthening Android’s Lead in Scam Protection**\\
\\
By\\
\\
\\
\\
Lyubov Farafonova\\
\\
\\
\\
&\\
\\
\\
Alberto Pastor Nieto\\
\\
\\
Feb 25, 2026](https://blog.google/security/staying-one-step-ahead-strengthening-androids-lead-in-scam-protection/)

.

Jump to position 1
Jump to position 2
Jump to position 3
Jump to position 4
Jump to position 5
Jump to position 6

Survey

Help us improve The Keyword with a one-question survey

YesNo

This survey is anonymous. All responses will be aggregated and used only for analysis to improve our services.

Did this article provide the level of detail you were looking for?

Yes, I got what I neededNo, I wanted more technical depthNo, I wanted a simpler overviewI was looking for something else entirely

✅

Thank you!