# PixelPop content

Stories, pictures and songs for PixelPop displays. A display downloads what it is missing from here on its own
(it reads `manifest.txt`); nobody has to press anything or run anything. Firmware and the Companion app live elsewhere.

* `nightnight/` : Night Night songs (`*.mp3`) and `tracks.txt` (title and credit for each). The songs are music-box
  renderings made for PixelPop of traditional melodies that are in the public domain.
* `storybook/<story>/` : the six narration files (`NN-name.mp3`) and twelve closeup pictures
  (`images/closeups/NN.jpg`) of each story. The tales are public-domain classics. The narration is a synthetic voice
  (OpenAI text-to-speech); say so wherever you present it. The pictures were made for PixelPop.

To add or change something, edit `data/` in the firmware repo and run `tools/build_content_repo.py`, or edit this repo
directly and regenerate `manifest.txt` with the same script. Only add material you have the right to redistribute:
this repository is public and every display fetches from it.
