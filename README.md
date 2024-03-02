# React Modal Component

A simple and customizable modal component for React applications.

## Installation

You can install the React Modal Component using npm. 

```bash
npm i @creedxd/modalcomponent
```
Usage
To use the modal component in your React application, follow these steps:

Import the Modal component into your file:

import Modal from 'react-modal-component';

Use the Modal component in your JSX:
```jsx
<Modal 
  isModalOpen={isModalOpen} 
  hanldeCloseModal={hanldeCloseModal} 
  modalText={"Your custom modal text here!"}
/>
```
Customize the content as needed.
Props
isModalOpen: (boolean) Indicates whether the modal is open or closed.
hanldeCloseModal: (function) Callback function to handle modal closing.
modalText: (string) Text content to be displayed within the modal.

Example
```jsx


import React, { useState } from 'react';
import Modal from 'react-modal-component';

function App() {
  const [isModalOpen, setIsModalOpen] = useState(false);

  const handleOpenModal = () => {
    setIsModalOpen(true);
  }

  const handleCloseModal = () => {
    setIsModalOpen(false);
  }

  return (
    <div>
      <button onClick={handleOpenModal}>Open Modal</button>
      <Modal 
        isModalOpen={isModalOpen} 
        hanldeCloseModal={handleCloseModal} 
        modalText={"Hello, this is a sample modal!"}
      />
    </div>
  );
}

export default App;
```