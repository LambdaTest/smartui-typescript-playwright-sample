# Run SmartUI TypeScript Playwright Tests on TestMu AI (Formerly LambdaTest)

<p align="center">
  <a href="https://www.testmuai.com/"><img src="https://img.shields.io/badge/MADE%20BY%20TestMu%20AI-000000.svg?style=for-the-badge&labelColor=000" alt="Made by TestMu AI"></a>
  <a href="https://community.testmuai.com/"><img src="https://img.shields.io/badge/Join%20the%20community-blueviolet.svg?style=for-the-badge&labelColor=000000" alt="Community"></a>
</p>

This sample demonstrates how to use TestMu AI (Formerly LambdaTest) Grid for running Playwright tests with TypeScript for SmartUI Visual Regression Testing.

## Prerequisites

- Node.js installed (version 14 or higher)
- NPM installed (version 7 or higher)
- A TestMu AI (Formerly LambdaTest) account

## Getting Started

[TestMu AI](https://www.testmuai.com/) (Formerly LambdaTest) is the world's first full-stack AI Agentic Quality Engineering platform that empowers teams to test intelligently, smarter, and ship faster. Built for scale, it offers a full-stack testing cloud with 10K+ real devices and 3,000+ browsers. With AI-native test management, MCP servers, and agent-based automation, TestMu AI supports Selenium, Appium, Playwright, and all major frameworks.

With TestMu AI (Formerly LambdaTest), you can run SmartUI TypeScript Playwright tests across real browsers and operating systems.

- [Sign up on TestMu AI](https://www.testmuai.com/register/) (Formerly LambdaTest).
- Follow the [TestMu AI Documentation](https://www.testmuai.com/support/docs/) for the full setup walkthrough.

Follow the steps below to set up and run the sample project.

### Step 1: Clone the repository

Clone this repository to your local machine.

```bash
git clone https://github.com/lambdatest/smartui-typescript-playwright-sample.git
```

### Step 2: Install dependencies

Navigate to the project directory and install the required dependencies using the following command:

```bash
cd smartui-typescript-playwright-sample
npm i
```

### Step 3: Set up credentials

Set up your TestMu AI (Formerly LambdaTest) username and access key as environment variables.

```bash
export LT_USERNAME="your_username"
export LT_ACCESS_KEY="your_accessKey"
```

Replace `your_username` and `your_accessKey` with your credentials.

### Step 4: SmartUI.takeScreenshot Webhook

In this sample, we have used the `smartui.takeScreenshot` webhook to capture a screenshot for visual regression testing. This webhook triggers a screenshot capture at the specified step in your test script.

When you use the `smartui.takeScreenshot` webhook, you can pass additional arguments such as `fullPage` and `screenshotName`. The `fullPage` argument indicates whether the screenshot should capture the entire page or just the viewport. The `screenshotName` argument allows you to provide a custom name for the screenshot. This name is used when saving the screenshot and displaying it in the SmartUI dashboard.

Here's an example of how to use the `smartui.takeScreenshot` webhook in your test script:

```typescript
await page.evaluate((_) => { },
    `lambdatest_action: ${JSON.stringify({ action: "smartui.takeScreenshot", arguments: { fullPage: true, screenshotName: "Your Screenshot Name" } })}`);
```

This line of code captures a full-page screenshot and saves it with the provided custom name. The captured screenshot will be available for review and comparison in your SmartUI dashboard.

By leveraging the `smartui.takeScreenshot` webhook in your test scripts, you can easily capture relevant screenshots at different stages of your test execution. This will help you detect and analyze visual differences across various browser and device combinations, and ensure that your web application looks and functions as expected.

### Step 5: Run the test

Run the test using the following command:

```bash
npm test
```

This will execute the test on TestMu AI (Formerly LambdaTest) Grid using Playwright with TypeScript, and SmartUI will capture a screenshot for visual regression testing.

## Conclusion

In this sample project, we demonstrated how to set up and run a SmartUI test using TestMu AI (Formerly LambdaTest) Grid for Playwright with TypeScript. You can now use this setup as a starting point for creating more complex tests and integrating them into your CI/CD pipeline.

## LambdaTest is Now TestMu AI

On **January 12, 2026**, [LambdaTest evolved to TestMu AI](https://www.testmuai.com/lambdatest-is-now-testmuai/), the world's first fully autonomous **Agentic AI Quality Engineering Platform**.

Same team. Same infrastructure. Same customer accounts. All existing LambdaTest logins, scripts, capabilities, and integrations continue to work without change.

ð Find the new home for [LambdaTest](https://www.testmuai.com).

### How LambdaTest Evolved into TestMu AI

In 2017, we launched LambdaTest with a simple mission: make testing fast, reliable, and accessible. As LambdaTest grew, we expanded into Test Intelligence, Visual Regression Testing, Accessibility Testing, API Testing, and Performance Testing, covering the full depth of the testing lifecycle.

As software development entered the AI era, testing had to evolve, too. We rebuilt the architecture to be AI-native from the ground up, with autonomous agents that **plan, author, execute, analyze, and optimize tests** while keeping humans in the loop. The platform integrates with your repos, CI, IDEs, and terminals, continuously learning from every code change and development signal.

That evolution earned a new name: **TestMu AI**, built for an AI-first future of quality engineering. TestMu is not a new name for us. It is the name of our annual community conference, which has brought together 100,000+ quality engineers to discuss how AI would reshape testing, long before that became an industry norm. 

What started as a high-performance cloud testing platform has transformed into an AI-native, multi-agent system powering a connected, end-to-end quality layer. That evolution defined a new identity: LambdaTest evolved into TestMu AI, built for an AI-first future of quality engineering.

## Support

Got a question? Email [support@testmuai.com](mailto:support@testmuai.com) or chat with us 24x7 from our chat portal.
