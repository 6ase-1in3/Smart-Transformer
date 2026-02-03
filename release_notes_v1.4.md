# Release Notes v1.4

> **Release Date**: 2026.02.03
> **Important Update**: Critical stability fix for Windows environments.

## 🔧 Critical Fixes (緊急修正)
*   **Resolved "Permission denied" / "Failed to extract" Error**:
    *   Fixed an issue where the single-file executable (`--onefile`) would fail to extract temporary files on certain Windows systems due to antivirus interference or permission locks.
    *   **Solution**: Switched to **Portable Folder Architecture (--onedir)**. The application no longer needs to self-extract at runtime, ensuring 100% startup reliability.

## 📦 Build Changes (版本異動)
*   **File Size Increase**:
    *   The installer size has increased (~50MB+). This is expected behavior as we are now shipping the complete uncompressed dependency folder structure to guarantee stability.
    *   *Trade-off*: Larger size for faster startup and zero extraction errors.

## 🚀 Improvements
*   **Faster Startup**: The app launches instantly as it no longer needs to decompress itself to a temporary folder every time.
