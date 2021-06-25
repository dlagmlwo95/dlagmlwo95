# Text-To-Speech

{% tabs %}
{% tab title="html" %}
```markup
    <div class="voiceinator">
      <h1>speak 버튼을 눌러보세요!</h1>

      <select name="voice" id="voices">
        <option value="">Select A Voice</option>
      </select>

      <label for="rate">Rate:</label>
      <input name="rate" type="range" min="0" max="3" value="1" step="0.1" />

      <label for="pitch">Pitch:</label>

      <input name="pitch" type="range" min="0" max="2" step="0.1" />
      <textarea name="text">hello! i love javascript</textarea>
      <button id="stop">Stop!</button>
      <button id="speak">Speak</button>
    </div>
```
{% endtab %}

{% tab title="javascript" %}
```javascript
      const msg = new SpeechSynthesisUtterance();
      let voices = [];
      const voicesDropdown = document.querySelector('[name="voice"]');
      const options = document.querySelectorAll(
        '[type="range"], [name="text"]'
      );
      const speakButton = document.querySelector("#speak");
      const stopButton = document.querySelector("#stop");
      msg.text = document.querySelector('[name="text"]').value;

      function populateVoices() {
        voices = this.getVoices();
        voicesDropdown.innerHTML = voices
          .filter((voice) => voice.lang.includes("ko"))
          .map(
            (voice) =>
              `<option value="${voice.name}">${voice.name} (${voice.lang})</option>`
          )
          .join("");
      }

      function setVoice() {
        msg.voice - voices.find((voice) => voice.name === this.valye);
        toggle();
      }

      function toggle(startOver = true) {
        speechSynthesis.cancel();
        if (startOver) {
          speechSynthesis.speak(msg);
        }
      }

      function setOption() {
        console.log(this.name, this.value);
        msg[this.name] = this.value;
        toggle();
      }
      speechSynthesis.addEventListener("voiceschanged", populateVoices);
      voicesDropdown.addEventListener("change", setVoice);
      options.forEach((option) => option.addEventListener("change", setOption));
      speakButton.addEventListener("click", toggle);
      stopButton.addEventListener("click", () => toggle(false));
```
{% endtab %}
{% endtabs %}

