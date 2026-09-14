class Node:
	def __init__(self, data):
		self.data = data
		self.previous = None
		self.next = None


class DeleteStart:
	def __init__(self):
		self.head = None
		self.tail = None

	def addNode(self, data):
		new_node = Node(data)
		if self.head is None:
			self.head = self.tail = new_node
			return

		self.tail.next = new_node
		new_node.previous = self.tail
		self.tail = new_node

	def deleteFromStart(self):
		if self.head is None:
			return

		if self.head is self.tail:
			self.head = self.tail = None
			return

		self.head = self.head.next
		self.head.previous = None

	def display(self):
		if self.head is None:
			print("List is empty")
			return

		current = self.head
		while current is not None:
			print(current.data)
			current = current.next
		print()


if __name__ == "__main__":
	d_list = DeleteStart()
	for value in range(1, 6):
		d_list.addNode(value)

	print("Original List:")
	d_list.display()
	while d_list.head is not None:
		d_list.deleteFromStart()
		print("Updated List:")
		d_list.display()
