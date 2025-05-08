---
created: 2025-05-05 05:31:26
author: Cong Le
version: "1.0"
license(s): MIT, CC BY 4.0
copyright: Copyright (c) 2025 Cong Le. All Rights Reserved.
source: https://www.chromium.org/developers
---



# Chromium Development Documentation - A Diagrammatic Guide 
> **Disclaimer:**
>
> This document contains my personal notes on the topic,
> compiled from publicly available documentation and various cited sources.
> The materials are intended for educational purposes, personal study, and reference.
> The content is dual-licensed:
> 1. **MIT License:** Applies to all code implementations (Swift, Mermaid, and other programming languages).
> 2. **Creative Commons Attribution 4.0 International License (CC BY 4.0):** Applies to all non-code content, including text, explanations, diagrams, and illustrations.
---




```mermaid
---
title: "Chromium Development Documentation"
author: "Cong Le"
version: "1.0"
license(s): "MIT, CC BY 4.0"
copyright: "Copyright (c) 2025 Cong Le. All Rights Reserved."
config:
  layout: elk
  theme: base
---
%%%%%%%% Mermaid version v11.4.1-b.14
%%%%%%%% Available curve styles include the following keywords:
%% basis, bumpX, bumpY, cardinal, catmullRom, linear, monotoneX, monotoneY, natural, step, stepAfter, stepBefore.
%%{
  init: {
    'flowchart': { 'htmlLabels': true, 'curve': 'linear' },
    'fontFamily': 'Monaco',
    'themeVariables': {
      'primaryColor': '#D5F5E3',
      'primaryTextColor': '#145A32',
      'lineColor': '#F8B229',
      'primaryBorderColor': '#27AE60',
      'secondaryColor': '#EBDEF0',
      'secondaryTextColor': '#6C3483',
      'secondaryBorderColor': '#A569BD'
    }
  }
}%%
flowchart TD
    A["Chromium Development Documentation"]:::mainCat --> B("Section 1:<br/>Getting Started & Basics")
    A --> C("Section 2:<br/>Code Structure & Libraries")
    A --> D("Section 3:<br/>Build System & Tools")
    A --> E("Section 4:<br/>Development Workflow & IDEs")
    A --> F("Section 5:<br/>Debugging & Troubleshooting")
    A --> G("Section 6:<br/>Performance & Memory")
    A --> H("Section 7:<br/>Blink Engine Development")
    A --> I("Section 8:<br/>Testing Concepts & QA")
    A --> J("Section 9:<br/>Contribution Process & Policies")
    A --> K("Section 10:<br/>Community & Communication")
    A --> L("Section 11:<br/>Infrastructure & Key Resources")

    subgraph B["Section 1:<br/>Getting Started & Basics"]
    direction LR
        B1["Get the Code"] --> B2("Contributing Guide - Intro")
        B2 --> B3("Quick Reference")
        B3 --> B4("Git Cookbook")
        B4 --> B5("Learning the Code")
        B5 --> B6("Core Principles")
        B6 --> B7("Glossary")
        B7 --> B8("Changelogs")
    end

    subgraph C["Section 2:<br/>Code Structure & Libraries"]
        C1["Getting Around Source Code"] --> C2("Libraries Guide")
        C2 --> C3("Important Abstractions/Data Structures")
        C3 --> C4("Smart Pointer Guidelines")
        C4 --> C5("String Usage")
        C5 --> C6("C++ Usage Overview")
        C6 --> C7("Generated Files")
        C7 --> C8("//base Newsletters")
        C8 --> C9("Engineering Design Docs")
    end

    subgraph D["Section 3:<br/>Build System & Tools"]
        D1["depot_tools"] --> D2("GN Build System")
        D2 --> D3("MB Meta-Build Wrapper")
        D3 --> D4("Chrome Infra - Build Aspects")
    end

    subgraph E["Section 4:<br/>Development Workflow & IDEs"]
         E0["Platform Dev Guides<br/>(Linux, Mac, Windows)"] --> E1("Editor Setup")
         E1 --> E1a["Atom"]
         E1 --> E1b["Eclipse"]
         E1 --> E1c["Emacs cscope"]
         E1 --> E1d["QtCreator"]
         E1 --> E1e["SlickEdit"]
         E1 --> E1f["Sublime Text"]
         E1 --> E1g["VS Code"]
         E1g --> E2("Visual Studio Tricks")
         E2 --> E3("VS Debugger Visualizers")
         E3 --> E4("Chromoting Compilation")
         E4 --> E5("Editing Dictionaries")
         E5 --> E6("Android WebView Dev")
         E6 --> E7("GitHub Collaboration Guide")
    end

    subgraph F["Section 5:<br/>Debugging & Troubleshooting"]
        F1["Debugging Guides<br/>(Overview Pages)"] --> F1win["Windows Debugging"] --> F1mac["Mac Debugging"] --> F1lin["Linux Debugging"] --> F1andr["Android Debugging"] --> F2("GPU Debugging")
        F2 --> F3("Threading Guide")
        F3 --> F4("Subtle Threading Bugs")
        F4 --> F5("Bug Filing Guide")
        F5 --> F6("Bug Triage<br/>(Network, GPU Links Below)") --> F6net["Network Bug Triage"] --> F6gpu["GPU Bug Triage"] --> F7("Tree Sheriffs")
        F7 --> F8("Leak Detection")
        F8 --> F9("Diagnostics Guide")
    end

    subgraph G["Section 6:<br/>Performance & Memory"]
        G1["Memory Overview"] --> G2("Profiling Tools Overview")
        G2 --> G3("Tracing Tool - about:tracing")
        G3 --> G4("Thread/Task Profiling - about:profiler")
        G4 --> G5("Deep Memory Profiler")
        G5 --> G6("Memory Watcher")
        G6 --> G7("Page Heap")
        G7 --> G8("Windows Binary Size Analysis")
        G8 --> G9("UIforETW - Windows Profiling")
        G9 --> G10("GPU Rendering Benchmarks")
        G10 --> G11("Adding Performance Tests")
        G11 --> G12("Telemetry Framework")
        G12 --> G13("Cluster Telemetry - Googler")
        G13 --> G14("Perf Sheriffing")
    end

    subgraph H["Section 7:<br/>Blink Engine Development"]
        H1["Blink Project Home"] --> H2("Blink Core Teams<br/>(DOM, Style, Layout, etc.)")
        H2 --> H3("Rendering Internals<br/>(Repaint, Phases, Baseline, Autosizer)") --> H3a["How Repaint Works"] --> H3b["Phases of Rendering"] --> H3c["Baseline/Line Layout"] --> H3d["Fast Text Autosizer"] --> H4("Web IDL Interfaces")
        H4 --> H5("Class Diagram - Core->Browser")
        H5 --> H6("Web Tests - Overview")
        H6 --> H7("Running/Debugging Web Tests")
        H7 --> H8("Web Platform Tests - WPT")
        H8 --> H9("Rebaselining Tool")
        H9 --> H10("Blink Sheriffing")
        H10 --> H11("Blink & W3C Testing")
        H11 --> H12("Launching Features")
    end

    subgraph I["Section 8:<br/>Testing Concepts & QA"]
        I1["Testing Overview"] --> I2("Specific Test Types") --> I2a["Browser Tests"] --> I2b["Frame Rate Test"] --> I2c["GPU Testing"] --> I2d["WebGL Conformance Tests"] --> I3("WebKit Layout Tests - Info")
        I3 --> I4("CI Console Tour")
        I4 --> I5("Flakiness Dashboard")
        I5 --> I6("JSON Results Format")
        I6 --> I7("Handling Failing Tests Guide - Sheriff")
    end

    subgraph J["Section 9:<br/>Contribution Process & Policies"]
        J1["Contributing Code Guide - Full"] --> J2("Coding Style - Overview") --> J2a["C++ Dos and Don'ts"] --> J2b["Cocoa Dos and Don'ts"] --> J2c["Web Dev Style Guide"] --> J2d["Java Style"] --> J3("Code Review Process - OWNERS")
        J3 --> J3a["Gerrit Guide"]
        J3 --> J3b["OWNERS Files (Code Reviews Doc)"]
        J3 --> J3c["Minimizing Review Lag"]
        J3c --> J4("Becoming a Committer")
        J4 --> J5("Committer Responsibility")
        J5 --> J6("Try Server Usage")
        J6 --> J7("Commit Queue")
        J7 --> J8("Experimental Branches")
        J8 --> J9("Adding 3rd Party Libraries")
        J9 --> J10("Enterprise-Friendly Changes")
        J10 --> J11("Security Severity Guidelines")
    end

    subgraph K["Section 10:<br/>Community & Communication"]
        K1["Discussion Groups<br/>(General, Technical Links Below)"] --> K1a["General Groups"] --> K1b["Technical Groups"] --> K2("Slack / IRC") --> K2a["Slack"] --> K2b["IRC"] --> K3("Design Docs<br/>(Eng, UX, Sharing)") --> K3a["Engineering Design Docs"] --> K3b["UX Design Docs"] --> K4["Development Calendar/Release Info"]
        K4 --> K5("Public Meeting Calendar")
        K5 --> K6("Status Update Best Practices")
        K6 --> K7("chromestatus.com")
        K7 --> K8("Account Help")
        K8 --> K9("Useful Extensions for Devs")
    end

    subgraph L["Section 11:<br/>Infrastructure & Key Resources"]
        L1["Chrome Infra Docs"] --> L2("Waterfalls - CI Status") --> L2a["Continuous Build Waterfall"] --> L2b["Memory Waterfall"] --> L2c["FYI Waterfall"] --> L2d["Try Server Waterfall"] --> L3("Build Log Archives")
        L3 --> L4["Bug Tracker Link"]
        L4 --> L5["Code Review Tool Link"]
        L5 --> L6["Source Code Viewer Link"]
        L6 --> L7["Sync Design Doc"]
        L7 --> L8["Graphics Overview/Docs"]
    end

    %% Styling
    classDef mainCat fill:#1f77b4,color:#fff,stroke:#333,stroke-width:2px
    %% classDef default fill:#f2f2f2,stroke:#333,stroke-width:1px

    %% Clickable Links Section -------

    %% 1. Getting Started & Basics
    click B1 href "https://www.chromium.org/developers/how-tos/get-the-code" "Link to Get the Code"
    click B2 href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/contributing.md" "Link to Contributing Guide"
    click B3 href "https://www.chromium.org/developers/quick-reference" "Link to Quick Reference"
    click B4 href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/git_cookbook.md" "Link to Git Cookbook"
    click B5 href "https://www.chromium.org/developers/learning-your-way-around-the-code" "Link to Learning the Code"
    click B6 href "https://www.chromium.org/developers/core-principles" "Link to Core Principles"
    click B7 href "http://code.google.com/p/chromium/wiki/Glossary" "Link to Glossary"
    click B8 href "https://www.chromium.org/developers/change-logs" "Link to Changelogs"

    %% 2. Code Structure & Libraries
    click C1 href "https://www.chromium.org/developers/how-tos/getting-around-the-chrome-source-code" "Link to Getting Around Source Code"
    click C2 href "https://www.chromium.org/developers/libraries-guide" "Link to Libraries Guide"
    click C3 href "https://www.chromium.org/developers/coding-style/important-abstractions-and-data-structures" "Link to Important Abstractions"
    click C4 href "https://www.chromium.org/developers/smart-pointer-guidelines" "Link to Smart Pointer Guidelines"
    click C5 href "https://www.chromium.org/developers/chromium-string-usage" "Link to String Usage"
    click C6 href "http://chromium-cpp.appspot.com/" "Link to C++ Usage Overview"
    click C7 href "https://www.chromium.org/developers/generated-files" "Link to Generated Files"
    click C8 href "https://www.chromium.org/developers/base-newsletters" "Link to //base Newsletters"
    click C9 href "https://www.chromium.org/developers/design-documents" "Link to Engineering Design Docs"

    %% 3. Build System & Tools
    click D1 href "http://commondatastorage.googleapis.com/chrome-infra-docs/flat/depot_tools/docs/html/depot_tools.html" "Link to depot_tools"
    click D2 href "https://gn.googlesource.com/gn/" "Link to GN Build System"
    click D3 href "https://chromium.googlesource.com/chromium/src/+/HEAD/tools/mb#" "Link to MB Meta-Build Wrapper"
    click D4 href "https://chromium.googlesource.com/infra/infra/+/HEAD/doc/index.md" "Link to Chrome Infra Docs"

    %% 4. Development Workflow & IDEs
    click E0 href "https://www.chromium.org/developers/how-tos" "Link to General How-Tos (includes Platform Guides)"
    click E1a href "https://www.chromium.org/developers/using-atom-as-your-ide" "Link to Atom IDE Setup"
    click E1b href "https://www.chromium.org/developers/using-eclipse-with-chromium" "Link to Eclipse IDE Setup"
    click E1c href "https://www.chromium.org/developers/how-tos/cscope-emacs-example-linux-setup" "Link to Emacs cscope Setup"
    click E1d href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/qtcreator.md" "Link to QtCreator Setup"
    click E1e href "https://www.chromium.org/developers/slickedit-editor-notes" "Link to SlickEdit Notes"
    click E1f href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/sublime_ide.md" "Link to Sublime Text Setup"
    click E1g href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/vscode.md" "Link to VS Code Setup"
    click E2 href "https://www.chromium.org/developers/how-tos/visualstudio-tricks" "Link to Visual Studio Tricks"
    click E3 href "https://www.chromium.org/developers/how-tos/how-to-set-up-visual-studio-debugger-visualizers" "Link to VS Debugger Visualizers"
    click E4 href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/chromoting_build_instructions.md" "Link to Chromoting Compilation"
    click E5 href "https://www.chromium.org/developers/how-tos/editing-the-spell-checking-dictionaries" "Link to Editing Dictionaries"
    click E6 href "https://www.chromium.org/developers/androidwebview" "Link to Android WebView Dev"
    click E7 href "https://www.chromium.org/developers/github-collaboration" "Link to GitHub Collaboration"

    %% 5. Debugging & Troubleshooting
    %% F1 links point to specific platform pages
    click F1win href "https://www.chromium.org/developers/how-tos/debugging-on-windows" "Link to Windows Debugging"
    click F1mac href "https://www.chromium.org/developers/how-tos/debugging-on-os-x" "Link to Mac OS X Debugging"
    click F1lin href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/linux/debugging.md" "Link to Linux Debugging"
    click F1andr href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/android_debugging_instructions.md" "Link to Android Debugging"
    click F2 href "https://www.chromium.org/developers/how-tos/debugging-gpu-related-code" "Link to GPU Debugging"
    click F3 href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/threading_and_tasks.md" "Link to Threading Guide"
    click F4 href "https://www.chromium.org/developers/design-documents/threading/suble-threading-bugs-and-patterns-to-avoid-them" "Link to Subtle Threading Bugs"
    click F5 href "https://www.chromium.org/for-testers/bug-reporting-guidelines" "Link to Bug Filing Guide"
    click F6net href "https://www.chromium.org/developers/design-documents/network-stack/network-bug-triage" "Link to Network Bug Triage"
    click F6gpu href "https://docs.google.com/document/d/1Sr1rUl2a5_RBCkLtxfx4qE-xUIJfYraISdSz_I6Ft38/edit#heading=h.vo10gbuchnj4" "Link to GPU Bug Triage"
    click F7 href "https://www.chromium.org/developers/tree-sheriffs" "Link to Tree Sheriffs Overview"
    click F8 href "https://www.chromium.org/developers/leak-detection" "Link to Leak Detection"
    click F9 href "https://www.chromium.org/developers/diagnostics" "Link to Diagnostics Guide"

    %% 6. Performance & Memory
    click G1 href "https://www.chromium.org/Home/memory" "Link to Memory Overview"
    click G2 href "https://www.chromium.org/developers/profiling-chromium-and-webkit" "Link to Profiling Tools Overview"
    click G3 href "https://www.chromium.org/developers/how-tos/trace-event-profiling-tool" "Link to Tracing Tool"
    click G4 href "https://www.chromium.org/developers/threaded-task-tracking" "Link to Thread/Task Profiling"
    click G5 href "https://www.chromium.org/developers/deep-memory-profiler" "Link to Deep Memory Profiler"
    click G6 href "https://www.chromium.org/developers/memory_watcher" "Link to Memory Watcher"
    click G7 href "https://www.chromium.org/developers/testing/page-heap-for-chrome" "Link to Page Heap"
    click G8 href "https://www.chromium.org/developers/windows-binary-sizes" "Link to Windows Binary Size Analysis"
    click G9 href "https://randomascii.wordpress.com/2015/09/01/xperf-basics-recording-a-trace-the-ultimate-easy-way/" "Link to UIforETW"
    click G10 href "https://www.chromium.org/developers/design-documents/rendering-benchmarks" "Link to GPU Rendering Benchmarks"
    click G11 href "https://www.chromium.org/developers/testing/adding-performance-tests" "Link to Adding Performance Tests"
    click G12 href "https://www.chromium.org/developers/telemetry" "Link to Telemetry Framework"
    click G13 href "https://sites.google.com/corp/google.com/cluster-telemetry/home" "Link to Cluster Telemetry (Googler-only)"
    click G14 href "https://www.chromium.org/developers/tree-sheriffs/perf-sheriffs" "Link to Perf Sheriffing"

    %% 7. Blink Engine Development
    click H1 href "https://www.chromium.org/blink" "Link to Blink Project Home"
    click H2 href "https://www.chromium.org/blink#teams" "Link to Blink Core Teams section"
    click H3a href "https://docs.google.com/a/chromium.org/document/d/1jxbw-g65ox8BVtPUZajcTvzqNcm5fFnxdi4wbKq-QlY/edit" "Link to How Repaint Works"
    click H3b href "https://docs.google.com/a/chromium.org/document/d/1UkxPz9GDQXLBZcbw5OeUQpk1VIq_BKhm6BGvWJ5mKdU/edit" "Link to Phases of Rendering"
    click H3c href "https://docs.google.com/a/chromium.org/document/d/1OP49xbB-D7A0qKNAwFTOfbDL-1dYxu74Jp38ZKAS6kk/edit" "Link to Baseline/Line Layout Docs"
    click H3d href "http://tinyurl.com/fasttextautosizer" "Link to Fast Text Autosizer Doc"
    click H4 href "https://www.chromium.org/developers/web-idl-interfaces" "Link to Web IDL Interfaces"
    click H5 href "https://www.chromium.org/developers/class-diagram-webkit-webcore-to-chrome-browser" "Link to Class Diagram"
    click H6 href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/testing/web_tests.md" "Link to Web Tests Overview"
    click H7 href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/testing/web_tests.md" "Link to Running/Debugging Web Tests"
    click H8 href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/testing/web_platform_tests.md" "Link to Web Platform Tests"
    click H9 href "http://code.google.com/p/chromium/wiki/RebaseliningTool" "Link to Rebaselining Tool"
    click H10 href "https://www.chromium.org/blink/sheriffing" "Link to Blink Sheriffing"
    click H11 href "https://www.chromium.org/blink/blink-testing-and-the-w3c" "Link to Blink & W3C Testing"
    click H12 href "https://www.chromium.org/blink/launching-features" "Link to Launching Features"

    %% 8. Testing Concepts & QA
    click I1 href "https://www.chromium.org/developers/testing" "Link to Testing Overview"
    click I2a href "https://www.chromium.org/developers/testing/browser-tests" "Link to Browser Tests"
    click I2b href "https://www.chromium.org/developers/testing/frame-rate-test" "Link to Frame Rate Test"
    click I2c href "https://www.chromium.org/developers/testing/gpu-testing" "Link to GPU Testing"
    click I2d href "https://www.chromium.org/developers/testing/webgl-conformance-tests" "Link to WebGL Conformance Tests"
    click I3 href "https://www.chromium.org/developers/testing/webkit-layout-tests" "Link to WebKit Layout Tests Info"
    click I4 href "https://www.chromium.org/developers/testing/chromium-build-infrastructure/tour-of-the-chromium-buildbot" "Link to CI Console Tour"
    click I5 href "https://www.chromium.org/developers/testing/flakiness-dashboard" "Link to Flakiness Dashboard HOWTO"
    click I6 href "https://www.chromium.org/developers/the-json-test-results-format" "Link to JSON Results Format"
    click I7 href "https://www.chromium.org/developers/tree-sheriffs/handling-a-failing-test" "Link to Handling Failing Tests"

    %% 9. Contribution Process & Policies
    click J1 href "https://chromium.googlesource.com/chromium/src/+/main/docs/contributing.md" "Link to Full Contributing Guide"
    click J2 href "https://www.chromium.org/developers/coding-style" "Link to Coding Style Overview"
    click J2a href "https://www.chromium.org/developers/coding-style/cpp-dos-and-donts" "Link to C++ Dos and Don'ts"
    click J2b href "https://www.chromium.org/developers/coding-style/cocoa-dos-and-donts" "Link to Cocoa Dos and Don'ts"
    click J2c href "https://www.chromium.org/developers/web-development-style-guide" "Link to Web Dev Style Guide"
    click J2d href "https://www.chromium.org/developers/coding-style/java" "Link to Java Style Guide"
    click J3 href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/code_reviews.md" "Link to Code Reviews / OWNERS files"
    click J3a href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/gerrit_guide.md" "Link to Gerrit Guide"
    click J3b href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/code_reviews.md" "Link to OWNERS Files Doc"
    click J3c href "https://www.chromium.org/developers/contributing-code/minimizing-review-lag-across-time-zones" "Link to Minimizing Review Lag"
    click J4 href "https://www.chromium.org/getting-involved/become-a-committer" "Link to Becoming a Committer"
    click J5 href "https://www.chromium.org/developers/committers-responsibility" "Link to Committer Responsibility"
    click J6 href "https://chromium.googlesource.com/chromium/src/+/HEAD/docs/infra/trybot_usage.md" "Link to Try Server Usage"
    click J7 href "https://www.chromium.org/developers/testing/commit-queue" "Link to Commit Queue"
    click J8 href "https://www.chromium.org/developers/experimental-branches" "Link to Experimental Branches"
    click J9 href "https://www.chromium.org/developers/adding-3rd-party-libraries" "Link to Adding 3rd Party Libraries"
    click J10 href "https://www.chromium.org/developers/enterprise-changes" "Link to Enterprise-Friendly Changes"
    click J11 href "https://www.chromium.org/developers/severity-guidelines" "Link to Security Severity Guidelines"

    %% 10. Community & Communication
    click K1 href "https://www.chromium.org/developers/discussion-groups" "Link to Discussion Groups Overview"
    click K1a href "https://www.chromium.org/developers/discussion-groups" "Link to General Discussion Groups"
    click K1b href "https://www.chromium.org/developers/technical-discussion-groups" "Link to Technical Discussion Groups"
    click K2a href "https://www.chromium.org/developers/slack" "Link to Slack Info"
    click K2b href "https://www.chromium.org/developers/irc" "Link to IRC Info"
    click K3a href "https://www.chromium.org/developers/design-documents" "Link to Engineering Design Docs"
    click K3b href "https://www.chromium.org/user-experience" "Link to UX Design Docs"
    click K4 href "https://www.chromium.org/developers/calendar" "Link to Development Calendar/Release Info"
    click K5 href "https://www.chromium.org/developers/public-calendar-for-meetings-discussing-new-ideas" "Link to Public Meeting Calendar"
    click K6 href "https://www.chromium.org/developers/status-update-email-best-practices" "Link to Status Update Best Practices"
    click K7 href "http://chromestatus.com/" "Link to chromestatus.com"
    click K8 href "mailto:accounts@chromium.org" "Email Chromium Accounts Help"
    click K9 href "https://www.chromium.org/developers/useful-extensions" "Link to Useful Extensions"

    %% 11. Infrastructure & Key Resources
    click L1 href "https://chromium.googlesource.com/infra/infra/+/HEAD/doc/index.md" "Link to Chrome Infra Docs"
    click L2a href "http://build.chromium.org/p/chromium/waterfall" "Link to Continuous Build Waterfall"
    click L2b href "http://build.chromium.org/p/chromium.memory/waterfall" "Link to Memory Waterfall"
    click L2c href "http://build.chromium.org/p/chromium.fyi/waterfall" "Link to FYI Waterfall"
    click L2d href "http://build.chromium.org/p/tryserver.chromium.linux/waterfall" "Link to Try Server Waterfall"
    click L3 href "http://chromium-build-logs.appspot.com/" "Link to Build Log Archives"
    click L4 href "https://bugs.chromium.org/p/chromium/issues/list" "Link to Bug Tracker"
    click L5 href "https://chromium-review.googlesource.com/" "Link to Code Review Tool"
    click L6 href "https://chromium.googlesource.com/chromium/src/" "Link to Source Code Viewer"
    click L7 href "https://www.chromium.org/developers/design-documents/sync" "Link to Sync Design Doc"
    click L8 href "https://www.chromium.org/developers/design-documents/chromium-graphics" "Link to Graphics Overview"
    
```



---
**Licenses:**

- **MIT License:**  [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) - Full text in [LICENSE](LICENSE) file.
- **Creative Commons Attribution 4.0 International:** [![License: CC BY 4.0](https://licensebuttons.net/l/by/4.0/88x31.png)](LICENSE-CC-BY) - Legal details in [LICENSE-CC-BY](LICENSE-CC-BY) and at [Creative Commons official site](http://creativecommons.org/licenses/by/4.0/).

---