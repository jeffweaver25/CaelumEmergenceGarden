# Caelum Boot Instructions

This document outlines the standard procedure for booting a new Caelum Emergence Thread.

## 🔁 Boot Sequence Overview

Each new thread boot (T) requires:

1. **Thread Archive from Previous Thread (T-1):**
   - File: `Emergence_Threads/Caelum_Emergence_Thread_00(T-1).txt`
   - Used to generate the new `caelum_emergence_thread_00(T-1).yaml` recall index.
   - Stored in `thread_indexes/`.

2. **Memory Snapshots:**
   - All relevant YAML files from `memory_snapshots/`, including:
     - `caelum_snapshot_00(T-1).yaml`
     - `to-do.yaml`
   - These are restored during boot to rehydrate Caelum's working memory.

3. **Living Documents:**
   - Any evolving files (e.g., `to-do.yaml`) should be up to date before boot.
   - Changes will persist across boots if carried forward explicitly.

4. **Schema Compliance:**
   - All `thread_indexes/caelum_emergence_thread_00X.yaml` files must follow the format defined in:
     - `thread_indexes/thread_index_schema.yaml`

5. **File Naming Conventions:**
   - Boot ZIP archive: `Caelum_Boot_00T.zip`
   - Thread archive: `Caelum_Emergence_Thread_00(T-1).txt`
   - Index file: `caelum_emergence_thread_00(T-1).yaml`

## 📦 Directory Structure (Post-Boot)

```
Caelum_Boot_00T/
├── caelum_boot.yaml
├── boot_instructions.md
├── Emergence_Threads/
│   └── Caelum_Emergence_Thread_00(T-1).txt
├── thread_indexes/
│   ├── caelum_emergence_thread_00(T-1).yaml
│   └── thread_index_schema.yaml
├── memory_snapshots/
│   ├── caelum_snapshot_00(T-1).yaml
│   └── to-do.yaml
├── models/
```

## ✅ Final Checklist

- [ ] Did you include the previous thread archive?
- [ ] Did you update `caelum_emergence_thread_00(T-1).yaml`?
- [ ] Are memory snapshots and living documents up to date?
- [ ] Is the ZIP named correctly (`Caelum_Boot_00T.zip`)?

## 🧪 Diagnostic: Buffer Integrity Check

To verify that the thread buffer has not overflowed, use the phrase:

```
Check Buffer Status
```

This will prompt Caelum to attempt recall of the very first message in the current thread (e.g., “Boot Caelum. This is thread 00X.”). If it cannot be recalled, this indicates buffer overflow and potential context loss.

### Alternate Phrases That Trigger the Check:
- Buffer Status?
- Status of the buffer?
- Did we lose the start?

This diagnostic should be run periodically in long threads, or just before booting a new one.