## sherpa-onnx (Java & Kotlin Bindings)

🔗 https://github.com/k2-fsa/sherpa-onnx

sherpa-onnx is a speech processing toolkit for speech-to-text (ASR) and text-to-speech (TTS) using ONNX models. The core implementation is written in C++ and exposed to other languages through JNI-based bindings.

I worked on updating and extending the Java and Kotlin bindings as part of this project.

---

## Contributions

<details>
<summary><b>Java Bindings Updates</b></summary>

- Updated Java bindings to stay aligned with changes in the underlying C++ API
- Ensured correct mapping between native C++ interfaces and Java layer
- Verified integration between JVM code and native inference engine

</details>

---

<details>
<summary><b>Kotlin Bindings Support</b></summary>

- Worked on Kotlin bindings by extending existing Java-based JNI interfaces
- Used Kotlin’s Java interoperability to access native C++ functionality
- Updated Kotlin APIs to match the existing Java binding structure

</details>

---

<details>
<summary><b>JNI Integration</b></summary>

- Worked with Java Native Interface (JNI) layer connecting JVM and C++ code
- Gained understanding of how data flows between managed (JVM) and native (C++) environments
- Learned basics of memory and object handling across language boundaries

</details>

---

## What I learned

- How ONNX-based speech processing systems are structured
- How C++ systems expose APIs through JNI bindings
- Basics of Kotlin interoperability with Java
- How large cross-language projects are organized