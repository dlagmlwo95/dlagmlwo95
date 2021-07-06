# Sorting Band Names

![](../../.gitbook/assets/image%20%2830%29.png)

{% tabs %}
{% tab title="HTML" %}
```markup
<ul id="bands"></ul>
```
{% endtab %}

{% tab title="JAVASCRIPT" %}
```javascript
      const bands = ['The Plot in You','The Devil Wears Prada', 'Pierce the Veil','Noram Jean','The bled', 'Say anything', 'The midway state', 'We came as romasns', 'Counterparts','Oh,sleeper','A skylit drive', 'Anywhere but here', 'An old dog'];

      function strip(bandName){
          return bandName.replace(/^(a |the |an )/i, '').trim();
      }
      const sortedBands = bands.sort((a,b) => strip(a) > strip(b) ? 1: -1);
      document.querySelector('#bands').innerHTML = sortedBands
      .map(band => `<li>${band}</li>`)
      .join('')

      console.log(sortedBands);
```
{% endtab %}
{% endtabs %}

