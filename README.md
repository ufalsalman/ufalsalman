Hi, this is Ufal.

I mainly using GitHub to host my project websites. I don't any fancy framework actually, just pure HTML, CSS and JS most of the time.

I am on [ufal.my.id](https://ufal.my.id) and you can contact me at [halo at ufal at my at id](mailto:halo@ufal.my.id)

<style>
  .now-playing {
  font-family: Arial, Helvetica, sans-serif;
  display: flex;
  flex-direction: row;
  align-items: center;
  max-width: 320px;
  border-radius: 10px;
  gap: 10px;
  background-color: #00000020;
  padding: 10px;
  border-radius: 10px;
  }

#albumLink {
  display: block;
  flex-shrink: 0;
}

#albumArt {
  width: 64px;
  height: 64px;
  border-radius: 6px;
  object-fit: cover;
}

.info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  text-align: left;
  overflow: hidden;
  flex: 1;
}

.now-playing-label {
  font-size: 0.7em;
  margin-bottom: 2px;
  font-weight: bold;
}

/* === Marquee === */
.scroll-rail {
  position: relative;
  width: 100%;
  overflow: hidden;
}

.scroll-track {
  display: inline-flex;
  align-items: center;
  gap: 32px;
  will-change: transform;
}

.marquee-running {
  animation: marquee linear infinite;
}

@keyframes marquee {
  from { transform: translateX(0); }
  to   { transform: translateX(calc(-1 * var(--marquee-distance))); }
}

.scroll-text {
  display: inline-block;
  font-weight: bold;
  font-size: 16px;
  line-height: 1.2em;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}

#trackMeta {
  font-size: 0.9em;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
</style>
<div class="now-playing" id="nowPlaying" style="display:none">
<a href="https://last.fm/user/ufalsalman" id="albumLink">
    <img decoding="async" src="" alt="Album Art" id="albumArt" />
</a>
                            
<div class="info">
    <div class="now-playing-label">Now Playing</div>

<div class="scroll-rail" id="titleRail">
<div class="scroll-track" id="titleTrack">
    <span id="trackTitle" class="scroll-text">Memuat…</span>
</div>
</div>

<div id="trackMeta"></div>
</div>
</div>

<script src="/lastfm/lastfmfetch.js"></script>
