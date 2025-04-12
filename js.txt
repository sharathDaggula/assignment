const noteTitle = document.getElementById("noteTitle");
const noteContent = document.getElementById("noteContent");
const noteTag = document.getElementById("addTag");

const bottomCardContainer = document.getElementById("cardContainer");



function createCardItem() {
    const cardItem = document.createElement("div");
    cardItem.classList.add("card-item-container");
    
    const cardTopItems = document.createElement("div");
    cardTopItems.classList.add("card-top-container");
    
    const headingElement = document.createElement("h1");
    headingElement.textContent = noteTitle.value;
    headingElement.classList.add("card-item-heading");
    cardTopItems.appendChild(headingElement);
    
    const iconEl = document.createElement("i");
    iconEl.id = "trashIcon";
    iconEl.classList.add("bi-trash");
    cardTopItems.appendChild(iconEl);
    
    cardItem.appendChild(cardTopItems);
    
    const contentElement = document.createElement("p");
    contentElement.textContent = noteContent.value;
    contentElement.classList.add("card-item-content");
    cardItem.appendChild(contentElement);
    
    const tagEl = document.createElement("p");
    tagEl.textContent = noteTag.value;
    tagEl.classList.add("card-item-tag");
    cardItem.appendChild(tagEl);
    
    bottomCardContainer.appendChild(cardItem);
    
    noteTitle.value="";
    noteContent.value="";
    noteTag.value="";
}
