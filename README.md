# react-beautiful-dnd

## 설치
`npm i react-beautiful-dnd`

## git
https://github.com/atlassian/react-beautiful-dnd

## DragDropContext
Drag and Drop 을 가능하게 하고자 하는 영역

## Droppable
드롭 가능한 영역

Droppable 안은 함수여야함



## Droggable
드래그 할 영역

### isDragDisabled
드래그 허용 여부를 제어


## 샘플
```
<DragDropContext onDragEnd={(e) => onDragEnd(e)}>
  <div>
    <Droppable droppableId="optionList">
      {(provided, snapshot) => (
        <div ref={provided.innerRef} {...provided.droppableProps}>
          {radioCkList.map((v, i) => {
            return (
              <Draggable
                draggableId={"draggable" + v.id}
                index={i}
                key={v.id}
              >
                {(provided, snapshot) => (
                  <div
                    key={v}
                    ref={provided.innerRef}
                    {...provided.draggableProps}
                    {...provided.dragHandleProps}
                  >
                    내용
                  </div>
                )}
              </Draggable>
            );
          })}
          {provided.placeholder}
        </div>
      )}
    </Droppable>
  </div>
</DragDropContext>
```
