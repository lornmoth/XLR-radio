# XLR-Radio Design Notes

## Goals

1. Personal use so I can avoid thinking what to put on
2. Moodsetting for xlr.pw tied to its active scheduling
3. Lack of existing automated internet radio with both strong curation and extensive content (doesn't repeat itself)
4. Demonstrate radio mixing is more effectively automated album-by-album over traditional singles format
5. Maintain ~2-hour thematic mixing standard without requiring high effort curation while still maintaining variability

## Automation Structure
- 24 HR Stream
  - Stream split into 6 two-hour blocks
    - Each Block contains 6 possible Playlists
    - Each Block split into 2 one-hour Segments that consists of one randomly chosen Playlist
      - Each Playlist contains <32 hours of music pertaining to a consistent sub-genre/theme
      - Each Playlist is made up of complete albums/EPS, which are selected randomly and played in full
      - Played album/ep's will be removed from the queue until the end of the Playlist
    - Next segment doesn't start until previous finishes current album after crossing the 1 hour mark
    - If current album finishes and there's less than 15 minutes before the next segment, skip to next segment
 
## Scheduling
The six scheduled blocks are designed to match the mood of a day as it graduates from morning to night. A side effect is the station is localized to its host.

**A. Morning:**
- 08 - 10 AM 
- 10 - 12 PM

**B. Noontime**
- 12 - 02 PM
- 02 - 04 PM

**C. Late Afternoon**
- 04 - 06 PM
- 06 - 08 PM

**D. Nighttime**
- 08 - 10 PM
- 10 - 12 AM

**E. Late Night**
- 12 - 02 AM
- 02 - 04 AM

**F. Early Morning**
- 04 - 06 AM
- 06 - 08 AM

## Programming
Cyclical: warm → cold, soft → hard, bright → dark, light → heavy; and back again

A. Minimalism: Japanese/German electronic minimalism
  1. Japanese Minimalism
  2. German minimalism
  3. Contemporary Classical minimalism
  4. 
B. World/Experimental
  1. Steel guitar
  2. Throat singing
  3. 
C. Light Techno
  1. Leftfield techno
  2. Hardware house
  3. Hardcore/jungle
  4.
D. Hard Techno: Industrial, Berlin, Acid
  1. Acid
  2. Industrial/Birmingham
  3. Berlin
  4.
E. Tekno:
  1. Tribal tekno
  2. Schranz
  3. Noise Techno
F. Noise:
  1. Field recordings
  2. Musique concrete
  3. 
  
## Implementation
Icecast, Foobar.

## Considerations
Consider removing segment system to allow 2-hour mixes for F, A & B due to the genres having a stronger album, not EP, emphasis which would usually occupy the entire 1 hour Segment. The block would end up being two theme-adjacent albums when two same-theme albums would be preferable.

Community voting on Playlist within Block. Do no expect many listeners, and only a small percent would bother engaging actively; this would allow those who care to push the stream in the direction they prefer, once an hour.
