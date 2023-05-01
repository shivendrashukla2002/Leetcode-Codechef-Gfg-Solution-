unordered_map<string,int> mm;
class Solution{
public:
    string help(Node* root){
        string temp = to_string(root->data);
        for(auto x:root->children){
            string t =help(x);
            temp = temp+t+"*";
        }
        mm[temp]++;
        return temp;
    }
    int duplicateSubtreeNaryTree(Node *root){
        // Code here
        mm.clear();
        help(root);
        int ans=0;
        for(auto x:mm){
            if(x.second>1)ans++;
        }
        return ans;
    }
};
