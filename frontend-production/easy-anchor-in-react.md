# Easy Anchor in React

Here is an easy way to have anchors in react using _scrollIntoView_

[https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollIntoView](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollIntoView)



```javascript
class Demo extends React.Component {
constructor(props){
    super(props);
    this.scrollToAnchor = this.scrollToAnchor.bind(this);
}
  
scrollToAnchor (anchorId){
  if (anchorId){   
  let anchorElement = document.getElementById(anchorId);
    if(anchorElement) {       
		  anchorElement.scrollIntoView();}
		}
  }
};

render(){
  return(
    <div>

      <button onClick={()=>(this.scrollToAnchor("target1"))}>
       Scroll Down To Target1
      </button>



      <div className="splash-content-two" id='target1'></div>
    </div>
  )
}}
```

