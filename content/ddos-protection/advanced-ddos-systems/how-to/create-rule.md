---
title: Create a rule
pcx_content_type: how-to
weight: 4
meta:
  title: Create an Advanced DDoS Protecton systems rule
---

# Create an Advanced DDoS Protection systems rule

Refer to the sections below to create a rule for Advanced TCP and DNS Protection.

## Create an Advanced TCP Protection rule

To create a [SYN flood rule](/ddos-protection/advanced-ddos-systems/overview/advanced-tcp-protection/#syn-flood-protection) or an [out-of-state TCP](/ddos-protection/advanced-ddos-systems/overview/advanced-tcp-protection/#out-of-state-tcp-protection) rule:

1. Log in to the [Cloudflare dashboard](https://dash.cloudflare.com) and select your account.
2. Go to **L3/4 DDoS** > **Advanced Protection** > **Advanced TCP Protection**.
3. Depending on the rule you are creating, do one of the following:

    * Under **SYN Flood Protection**, select **Create SYN flood rule**.
    * Under **Out-of-state TCP Protection**, select **Create out-of-state TCP rule**.

4. In **Mode**, select a [mode](/ddos-protection/advanced-ddos-systems/rule-settings/#mode) for the rule.
5. Under **Set scope**, select a [scope](/ddos-protection/advanced-ddos-systems/rule-settings/#scope) for the rule. If you choose to apply the rule to a subset of incoming packets, select a region or a data center.
6. Under **Sensitivity**, define the [burst sensitivity](/ddos-protection/advanced-ddos-systems/rule-settings/#burst-sensitivity) and [rate sensitivity](/ddos-protection/advanced-ddos-systems/rule-settings/#rate-sensitivity) of the rule (by default, _Medium_). The sensitivity levels are based on the initially configured thresholds for your specific case.
7. Select **Deploy**.

{{<render file="_atp-filters-rules-precedence.md">}}

## Create an Advanced DNS Protection rule

1. Contact your account team to enable Advanced DNS Protection and make the initial configuration. The initial thresholds are based on your network’s individual behavior.
2. Log in to the [Cloudflare dashboard](https://dash.cloudflare.com/login) and select your account. 
3. Go to **L3/4 DDoS** > **Advanced Protection** > **General settings**.
4. Add the prefixes you wish to onboard. Advanced DNS Protection will only be applied to the prefixes you onboard. If you already onboarded the desired prefixes when you configured Advanced TCP Protection, you do not need to take any other action.

    {{<Aside type="note" header="Note">}}
Currently, the list of onboarded prefixes is shared with Advanced TCP Protection. Any onboarded prefixes will be subject to both Advanced TCP Protection and Advanced DNS Protection, assuming that your account team has done the initial configuration of both systems. However, you can leave Advanced TCP Protection in monitoring mode.
    {{</Aside>}}

5. Go to **Advanced DNS Protection**. 
6. Select **Create Advanced DNS Protection rule**. 
7. In **Mode**, select a mode for the rule.
8. Under **Set scope**, select a [scope](/ddos-protection/advanced-ddos-systems/rule-settings/#scope) to determine the range of packets that will be affected by the rule. 
9. Under **Sensitivity**, define the [burst sensitivity](/ddos-protection/advanced-ddos-systems/rule-settings/#burst-sensitivity), [rate sensitivity](/ddos-protection/advanced-ddos-systems/rule-settings/#rate-sensitivity), and [profile sensitivity](/ddos-protection/advanced-ddos-systems/rule-settings/#profile-sensitivity) to determine when to initiate mitigation. 
10. Select **Deploy**.