# Drum Kit in Vanilla

![](../../.gitbook/assets/image%20%2823%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
<div class="keys">
      <div data-key="65" class="key">
        <kbd>A</kbd>
        <span class="sound">clap</span>
      </div>
      <div data-key="83" class="key">
        <kbd>S</kbd>
        <span class="sound">hihat</span>
      </div>
      <div data-key="68" class="key">
        <kbd>D</kbd>
        <span class="sound">kick</span>
      </div>
      <div data-key="70" class="key">
        <kbd>F</kbd>
        <span class="sound">openhat</span>
      </div>
      <div data-key="71" class="key">
        <kbd>G</kbd>
        <span class="sound">boom</span>
      </div>
      <div data-key="72" class="key">
        <kbd>H</kbd>
        <span class="sound">ride</span>
      </div>
      <div data-key="74" class="key">
        <kbd>J</kbd>
        <span class="sound">snare</span>
      </div>
      <div data-key="75" class="key">
        <kbd>K</kbd>
        <span class="sound">tom</span>
      </div>
      <div data-key="76" class="key">
        <kbd>L</kbd>
        <span class="sound">tink</span>
      </div>
    </div>

    <audio data-key="65" src="sounds/clap.wav"></audio>
    <audio data-key="83" src="sounds/hihat.wav"></audio>
    <audio data-key="68" src="sounds/kick.wav"></audio>
    <audio data-key="70" src="sounds/openhat.wav"></audio>
    <audio data-key="71" src="sounds/boom.wav"></audio>
    <audio data-key="72" src="sounds/ride.wav"></audio>
    <audio data-key="74" src="sounds/snare.wav"></audio>
    <audio data-key="75" src="sounds/tom.wav"></audio>
    <audio data-key="76" src="sounds/tink.wav"></audio>

```
{% endtab %}

{% tab title="CSS" %}
```css
      .key {
          float:left;
        border: 4px solid black;
        border-radius: 5px;
        margin: 1rem;
        font-size: 1.5rem;
        padding: 1rem 0.5rem;
        transition: all 0.07s;
        width: 100px;
        text-align: center;
        color: white;
        background: rgba(0, 0, 0, 0.4);
        text-shadow: 0 0 5px black;
      }
      .playing {
        transform: scale(1.1_);
        border-color: #ffc600;
        box-shadow: 0 0 10px #ffc600;
      }
      kbd {
        display: block;
        font-size: 40px;
      }
      .sound {
        font-size: 1.2rem;
        text-transform: uppercase;
        letter-spacing: 1px;
        co
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
    <script>
      function playSound(e) {
        const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
        const key = document.querySelector(`.key[data-key="${e.keyCode}"]`);
        if (!audio) return; // stop the function form running all together(함수실행중지)
        audio.currentTime = 0; // start
        audio.play();
        key.classList.add("playing");
      }

      function removeTransition(e) {
        if (e.propertyName !== "transform") return;
        this.classList.remove("playing");
      }

      const keys = document.querySelectorAll("key");
      keys.forEach((key) => key.addEventListener("transitionend", ramoveTransition));
      window.addEventListener("keydown".playSound);
    </script>
```
{% endtab %}
{% endtabs %}



