class Node:
	def __init__(self, data):
		self.data = data
		self.next = None
		self.prev = None


class DoublyLinkedList:
	def __init__(self):
		self.head = None

	def push(self, new_data):
		new_node = Node(new_data)
		new_node.next = self.head
		if self.head is not None:
			self.head.prev = new_node
		self.head = new_node

	def insertAfter(self, prev_node, new_data):
		if prev_node is None:
			print("The given previous node cannot be NULL")
			return

		new_node = Node(new_data)
		new_node.next = prev_node.next
		prev_node.next = new_node
		new_node.prev = prev_node
		if new_node.next is not None:
			new_node.next.prev = new_node

	def append(self, new_data):
		new_node = Node(new_data)
		if self.head is None:
			self.head = new_node
			return

		last = self.head
		while last.next is not None:
			last = last.next
		last.next = new_node
		new_node.prev = last

	def printList(self, node):
		if node is None:
			print("List is empty")
			return

		print("\nTraversal in forward direction")
		last = None
		while node is not None:
			print(node.data)
			last = node
			node = node.next

		print("\nTraversal in reverse direction")
		while last is not None:
			print(last.data)
			last = last.prev


if __name__ == "__main__":
	linked_list = DoublyLinkedList()
	linked_list.append(6)
	linked_list.push(7)
	linked_list.push(1)
	linked_list.append(4)
	linked_list.insertAfter(linked_list.head.next, 8)
	print("Created DLL is:")
	linked_list.printList(linked_list.head)
