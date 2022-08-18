# Merge_List_of_Dictionaries_Python
Python : Merge List of Dictionaries Python (Same ID)


    data_one = [{'id': 1, 'name': 'Kasun', 'Address': 'Galle'}, ]
    data_two = [{'id': 1, 'subject': 'Chemistry', 'marks': 70}, ]

      def merge_lists(l1, l2, key):
          merged = {}
          for item in l1 + l2:
              if item[key] in merged:
                  merged[item[key]].update(item)
              else:
                  merged[item[key]] = item
          return merged.values()

   
      dataform = merge_lists(data_one, data_two, 'id')
      print(dataform)
      
      
#output

    dict_values([{'id': 1, 'name': 'Kasun', 'Address': 'Galle', 'subject': 'Chemistry', 'marks': 70}])
