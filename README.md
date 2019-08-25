# program_study
def printTable(tabledate):
    colwidth = [] * len(tableData)

    for data in tableData:
        data_len = []
        for d in data:
            data_len.append(len(d))
        colwidth.append(max(data_len))

    colwidth_max = max(colwidth)

    for t in range(len(tableData[0])):
        for i in range(len(tableData)):
            print(tableData[i][t].rjust(colwidth_max), end='')
        print('\t')


tableData = [['apples', 'oranges', 'cherries', 'banana'],
             ['Alice', 'Bob', 'Carol', 'David'],
             ['dogs', 'cats', 'moose', 'goose']]

printTable(tableData)
