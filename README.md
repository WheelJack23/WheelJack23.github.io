### WheelJack

Null pointer dereference is a common and serious type of bug, which raises Null Pointer Exceptions (NPEs).There are two groups of approaches to detect NPEs. Type-based approaches carry out strict type-based null safety checking. They heavily rely on annotations, and thus produce many false positives. Dataflow-based approaches leverage static forward and/or backward dataflow analysis. They mostly have a limited capability in tracking fields and interprocedural analysis, and introduce false positives and false negatives.

To address these drawbacks, we propose WheelJack to detect NPEs for Java. It does not rely on annotations, and hence can work effectively under a lack of annotations. It leverages our novel abstraction of nullness status to enhance field tracking, and our novel invocation analysis (capturing change to return value and side effect of an invocation) to enhance interprocedural analysis.Our evaluation on 28 Java projects has demonstrated that WheelJack can mostly outperform the four state-of-the-art NPE detectors in recall without sacrificing precision. 5 and 2 new NPEs have been confirmed and fixed by developers after we submit 8 issues.

The paper has been submitted to ICSME 2023. See our [data](data.zip), [code](https://github.com/WheelJack23/WheelJack23.github.io/raw/main/code.zip) and [program analysis property comparison](tool-comparison.zip).
