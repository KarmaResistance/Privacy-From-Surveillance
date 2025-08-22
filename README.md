# Privacy-From-Surveillance

## Why This Project Exists

If you come from a poor or middle-class family, freedom of speech and human rights are often the only protections you have. So why not defend them as much as you can?

You could be a journalist, a civilian, or anyone who dares to speak the truth. If you live under an authoritarian state or in a country that is sliding toward authoritarianism, where government surveillance threatens your life or the lives of your loved ones simply because of your criticism, then this project shows a method to safely communicate and share files with people that you care without exposing yourself to unnecessary risks.

## Project Requirements

Hardware
- A laptop or desktop with USB boot capability
- At least one USB drive (8 GB or larger) for installing Tails OS

Operating System & Tools
- Tails OS (latest stable version)
- Tor Browser (included in Tails)
- OnionShare (included in Tails)
- Steghide (optional)
- Briar (Android app, optional)

Software
- Rufus (for writing Tails to USB)

## What This Project Demonstrates

This project is not about hacking or illegal activity. Instead, it demonstrates practical techniques for censorship-resistant and anonymous communication, inspired by how people in restrictive environments protect their freedom of expression.

The project covers four main areas:

1. Anonymous Operating System (Tails OS)
 - Running a live, amnesic operating system from USB.
 - Leaves no trace on the host machine.
 - All Internet connections are forced through Tor.

2. Secure File Sharing (OnionShare)
 - Create temporary Tor-based file-sharing services.
 - Send or receive documents without using centralized servers.
 - No metadata leaks (like IP addresses or accounts).

3. Decentralized Messaging (Briar)
 - Peer-to-peer messaging app that works over Tor, Wi-Fi, or even Bluetooth.
 - Useful in environments where the Internet is censored or shut down.
 - Designed for journalists, activists, and citizens under surveillance.
   
4. Steganography (Steghide) (Optional)
 - Hiding sensitive messages inside harmless-looking files (e.g., images, MP3s).
 - Only someone with the correct passphrase can extract the hidden content.
 - Demonstrates how information can be disguised to bypass censorship.

## Steps

1. Prepare the Environment
- Download the Tails OS ISO from the official site: https://tails.net/install/index.en.html
- Verify the ISO.
- Install Tails onto a USB drive using Rufus.
- Boot from the USB and start the Tails.
- I recommend you to NOT turn on the 'persistence storage'. KEEP IT TURNED OFF.
- If you want visual guidance, watch and follow the steps takes in this video : https://www.youtube.com/watch?v=xLX-SyJLeKA

2. Steganography with Steghide (Optional)
   
Steghide is used to hide documents inside images or audio files, making them look harmless. For example, a PDF file can be embedded inside a holiday photo. Only someone with the right passphrase can extract it. Do note that there are image-based, audio & video based, text based and network based. I did image and audio based. You can steghide your documents before you send them to anyone thorugh OnionShare.

- Open a terminal in Tails.
  
- Install steghide with these commands :

```  
sudo apt update
sudo apt install steghide
```

- Embed a file inside an image or audio (PDF inside JPG or WAV) with these commands:
  
```
steghide embed -cf cover.jpg -ef secret.pdf -sf output.jpg
```

(You will set a passphrase.)
  
- To extract the file later:

```  
steghide extract -sf output.jpg
```

- Only someone with the passphrase can recover the hidden content.
- Use AI tools like ChatGPT if you want guidance.

3. Secure File Sharing with OnionShare
- In Tails, open OnionShare.
- Choose “Share Files” or “Receive Files.”
- Drag and drop the files you want to share.
- OnionShare will generate a .onion link.
- Send this link securely to the receiver (can be via Briar or in person).
- The receiver opens the link using Tor Browser to download the files.
- Visual guidance : https://www.youtube.com/watch?v=gCDbHkpkNJ0 

4. Private Messaging with Briar
- Download Briar (Android only) from playstore.
- On both sender and receiver devices:
  
- `Install Briar`.

- `Exchange QR codes in person` (for maximum security).

- `Start chatting over Tor, Wi-Fi or Bluetooth`.

- Use Briar for text communication when files aren’t needed.
- Visual guidance : https://www.youtube.com/watch?v=rI2y3PnqRCI

5. Combine the Tools
- Draft sensitive text or documents offline.
- Hide them inside images or audios (Steghide).
- Share them safely with OnionShare.
- Use Briar for coordination and back-channel communication.
- Always run everything inside Tails OS for anonymity.




