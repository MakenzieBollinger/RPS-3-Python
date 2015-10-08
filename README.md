# RPS-3-Python

def getThrowToBeat(array, item):
	rockCount = 0
	scissorCount = 0
	paperCount = 0
	for i in range(len(array)):
		if array[i] == item:
			temp = array[i+1]
			if temp == "P":
				paperCount = paperCount + 1
			elif temp == "R":
				rockCount = rockCount + 1
			elif temp == "S":
				scissorCount = scissorCount + 1
	if rockCount > scissorCount and rockCount > paperCount:
		retun "R"
	elif scissorCount > rockCount and scissorCount > paperCount:
		return "S"
	elif paperCount > scissorCount and paperCount > rockCount:
		return "P"
	lastIndex = getLastIndexOf(array, item)
