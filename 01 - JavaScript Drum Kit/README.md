# Day-1

### 1. keydown => playSound
```
function playSound(e){
  const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);

  if(!audio){
    return
  }
  audio.currentTime = 0;
  audio.play();
}

window.addEventListener('keydown', playSound);
```


### 2. keydown => css-style change

```
const key = document.querySelector(`div[data-key="${e.keyCode}"]`);
key.classList.add('playing');
```

###　3. css-style remove
```
function removeTransition(e){
  if(e.propertyName != 'transform') return;
  e.target.classList.remove('playing');
}

const keys = document.querySelectorAll('.key');
keys.forEach(element => {
  element.addEventListener('transitionend', removeTransition);
})
```
