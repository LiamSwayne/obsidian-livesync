### 0.20.0

At 0.20.0, Self-hosted LiveSync has changed the binary file format and encrypting format, for efficient synchronisation.  
The dialogue will be shown and asks us to decide whether to keep v1 or use v2. Once we have enabled v2, all subsequent edits will be saved in v2. Therefore, devices running 0.19 or below cannot understand this and they might say that decryption error. Please update all devices.  
Then we will have an impressive performance.

Of course, these are very impactful changes. If you have any questions or troubled things, please feel free to open an issue and mention me.

Note: if you want to roll it back to v1, please enable `Use binary and encryption version 1` on the `Hatch` pane and perform the `rebuild everything` once.

Extra but notable information:

This format change gives us the ability to detect some `marks` in the binary files as same as text files. Therefore, we can split binary files and some specific sort of them (i.e., PDF files) at the specific character. It means that editing the middle of files could be detected with marks.

Now only a few chunks are transferred, even if we add a comment to the PDF or put new files into the ZIP archives.

#### Version history
- 0.20.2
  - New feature:
    - We can delete all data of customization sync from the `Delete all customization sync data` on the `Hatch` pane.
  - Fixed:
    - Prevent keep restarting on iOS by yielding microtasks.
- 0.20.1 
  - Fixed:
    - No more UI freezing and keep restarting on iOS.
    - Diff of Non-markdown documents are now shown correctly.
  - Improved:
    - Performance has been a bit improved.
    - Customization sync has gotten faster.
      - However, We lost forward compatibility again (only for this feature). Please update all devices.
  - Misc
    - Terser configuration has been more aggressive.
- 0.20.0
  - Improved:
    - A New binary file handling implemented
    - A new encrypted format has been implemented
    - Now the chunk sizes will be adjusted for efficient sync
  - Fixed:
    - levels of exception in some logs have been fixed
  - Tidied:
    - Some Lint warnings have been suppressed.

... To continue on to `updates_old.md`.
