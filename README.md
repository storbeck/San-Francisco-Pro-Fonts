Here’s a **simple and clean README** for your GitHub font collection:

---

# **SF Pro Fonts for Linux**  
A simple guide to extracting and installing Apple’s **SF Pro** fonts on Linux.

## **📥 Download and Extract**  
1. **Download the fonts** from Apple's official site:  
   [https://developer.apple.com/fonts/](https://developer.apple.com/fonts/)  
2. Extract the `.dmg` file:  
   ```sh
   7z x SF-Pro.dmg -oSFProExtracted
   ```
3. Extract the `.pkg` file:  
   ```sh
   cd SFProExtracted
   7z x "SF Pro Fonts.pkg" -oSFProFonts
   ```
4. Extract the `Payload` file:  
   ```sh
   cd SFProFonts
   cpio -idmv < Payload~
   ```
5. Fonts will be in `Library/Fonts/`.

## **💾 Install on Linux**  
1. Move the fonts to your local font directory:  
   ```sh
   mkdir -p ~/.local/share/fonts
   cp -r Library/Fonts/*.otf ~/.local/share/fonts/
   ```
2. Update the font cache:  
   ```sh
   fc-cache -fv
   ```

## **🖥️ Optional: Set as System Font**  
- Use **GNOME Tweaks** or your desktop environment’s font settings.  
