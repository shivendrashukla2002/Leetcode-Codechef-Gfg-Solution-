class TrieNode {
    TrieNode[] children;
    boolean isEndOfWord;
    TrieNode(){
        isEndOfWord=false;
        children = new TrieNode[26];
    }
}

class Solution
{
    public int klengthpref(String[] arr, int n, int k, String str)
    {
        // code here
        int count=0;
        // TrieNode root = new TrieNode();
        if(k>str.length()){
            return count;
        }
        String sub=str.substring(0,k);
        for(String word:arr){
            if(k>word.length()){
                continue;
            }
            TrieNode root = new TrieNode();
            create(root, word.substring(0,k));
            if(search(root, sub)){
                count+=1;
            }
        }
        
        return count;
    }
    
    public void create(TrieNode root, String word){
        TrieNode currNode = root;
        for(int idx=0; idx<word.length(); idx++){
            char currChar = word.charAt(idx);
            if(currNode.children[currChar-'a']==null){
                TrieNode newNode = new TrieNode();
                currNode.children[currChar - 'a']=newNode;
            }
            currNode = currNode.children[currChar-'a'];
        }
        currNode.isEndOfWord=true;
    }
    
    public boolean search(TrieNode root, String key){
        TrieNode currNode = root;
        for(int idx=0; idx<key.length(); idx++){
            char currChar = key.charAt(idx);
            if(currNode.children[currChar-'a']==null) return false;
            currNode = currNode.children[currChar-'a'];
        }
        return currNode.isEndOfWord;
    }
}
