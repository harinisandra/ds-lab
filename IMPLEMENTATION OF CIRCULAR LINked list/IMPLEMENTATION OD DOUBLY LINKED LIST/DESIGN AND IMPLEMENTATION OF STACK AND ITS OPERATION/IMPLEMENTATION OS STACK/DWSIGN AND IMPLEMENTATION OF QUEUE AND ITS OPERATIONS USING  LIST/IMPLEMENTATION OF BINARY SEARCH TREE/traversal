INT_MIN = -2**32


def canRepresentBST(preorder):
	stack = []
	lower_bound = INT_MIN

	for value in preorder:
		if value < lower_bound:
			return False

		while stack and stack[-1] < value:
			lower_bound = stack.pop()

		stack.append(value)

	return True


if __name__ == "__main__":
	preorder_one = [40, 30, 35, 80, 100]
	preorder_two = [40, 30, 35, 20, 80, 100]

	print("true" if canRepresentBST(preorder_one) else "false")
	print("true" if canRepresentBST(preorder_two) else "false")
