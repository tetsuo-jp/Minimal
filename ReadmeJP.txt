        Minimal ���p�҃}�j���A�� (V1.0)

���̃}�j���A���͎O�̕����ɕ�����Ă���B

  1. ���̓��[�v�̎g����
        Minimal�̊�{�I�Ȏg�p�@

  2. �l�A���s�Ɛ���\��
        ����ň����T�O�ׂ̍�����`

  3. �g���֐�
        �񋟂���Ă���֐��̃��X�g
        ��g���X�́u�R���s���[�^�T�C�G���X����v�ɔ�ׂāA�������֐�
        ���ǉ�����Ă���B
          �r�b�g���Z�q   land lor lxor lsl lsr
          ���o��         read_file write_file
          �ϊ�           int_of_string float_of_string round format_float
          �V�X�e����     require system time
          �O���t�B�b�N�X point_color   

�T���v���v���O��������������������Ă���B
    prelude.mal
       ���ʂ֗̕��Ȋ֐��B���̃T���v������悭`require "prelude";'�Ƃ�
      ���`�ŗ��p����Ă���
    variable.mal, stack.mal, queue.mal, btree.mal
       �悭����f�[�^�\���̎�����
    poly.mal, matrix.mal  ���w�I�ȍ\��
    int32.mal             32�r�b�g�����̏���
    music.mal             �����ȃs�A�m
    graphics.mal          �֐��O���t��`�����߂̃c�[��
    turtle.mal            �^�[�g���𓮂����ĊG��`���܂��傤


1. ���̓��[�v�̎g����

  Minimal �͑��̑����̃v���O���~���O����ƈႢ�A�v���O�������R���p�C��
  ���āA���s����̂ł͂Ȃ��B���̓��[�v���g���AMinimal�ƑΘb���Ȃ���A
  �l��֐����`������A�����v�Z�E���s�����肷��̂��B�v���O������P��
  �Ƃ�������A���̂�肩���ł͊֐���A���S���Y���̓���m�F���e�Ղɂ�
  ���邽�߂��B

a) �����グ�ƏI��
  ���̑Θb�I���̓��[�v�ɓ��邽�߂ɁA�܂�DOS����UNIX����Minimal�𗧂���
  ����B(Minimal���N���b�N���Ă�����)

        C:\MINIMAL> minimal
        >       MiniMAL version 1.0 (SJIS) on Objective Caml
        
        # 

  �Ō�� # �̓v�����v�g�ƌ����A���͑҂���\���Ă���B

  ���̓��[�v����o�����Ƃ��Aquit(); �Ɠ��͂��ĉ������B

        # quit();
        C:\MINIMAL>

b) ����
  ���̓��[�v�ŉ�������͂���B�Ⴆ�� "1+2;<CR>"

        # 1+2;
        - : int = 3

  ";" �� Minimal �ɓ��͂��I��������Ƃ�m�点��B���ꂪ�Ȃ��ƁA<CR>��
  ��������A���s���Ă����͂������B

  "- : int = 3" �� Minimal �̓������B
  "-" �͓��͂��ꂽ�������̂܂܎��s���ꂽ���Ƃ�\���B
  "int" �͓��͂��ꂽ���������^���������Ƃ�\���B���[�U�����͂���K�v��
  �Ȃ��AMinimal�������I�ɂ�����v�Z���Ă����B
  "3" �͎��s�̌��ʂ��B

c) �l�Ɗ֐��̒�`
  �l���`����Ɠ�����������ƈႤ�B

        # val x = 2*2;
        val x : int = 4

  x �͒�`���ꂽ�l�̖��O�ŁAint �͂��̌^�ŁA������ 4 �� x �̐V�����l��
  ����B���̌� x �����̒��ɏ����ƁA���̒l�� 4 �ɂȂ�B

        # x+1;
        - : int = 5

  �֐��̒�`�͓��l�ȕ\���ɂȂ�B

        # fun f x = x+1;
        val f : int -> int = <fun>

  Minimal �͊֐��^����Ȃ̂ŁA�֐��͕��ʂ̒l�ł���B������A�l�̒�`��
  ���l�ɓ��� "val" �Ŏn�܂�B�^�͐������琮���ւ̊֐��Ȃ̂ŁA"int ->
  int"�B�֐��̒l�͕\���ł��Ȃ��̂ŁA�l�̏��� "<fun>" �ɂȂ��Ă���B

d) �ϐ��̒�`
  Minimal �ɂ͒l�̒�`�Ƃ�����ƈႤ�ϐ��̒�`������B

        # var x = 1;
        var x : int = 1

  �ϐ��͒l�Ǝg������������肷��̂ŁA���� "val" �ł͂Ȃ� "var" �ɂȂ�
  ���B�l�Ɠ��l�ɁA�ϐ��͂��̌�̎��̒��Ɏg���邪�A�l�ƈႢ�A���̒��g��
  �ς�����B

        # x;
        - : int = 1
        # x <- 5;
        - : unit = ()
        # x;
        - : int = 5

  "x <- 5" �� x ���`����̂ł͂Ȃ��A���ɒ�`���ꂽ�����̕ϐ� x �̒�
  �g��ς���B
  ���̓��� "- : unit = ()" �͓��ɈӖ����Ȃ��Bunit �^�ɂ͂�����̒l 
  "()" �����܂܂ꂸ�A���Ɍ��ʂ��Ȃ��Ƃ��͂����Ԃ��B

  ��`����Ă��Ȃ��ϐ��ɒl�����悤�Ƃ�����A�ϐ��̌^�ƈႤ�^�̒l���
  ��悤�Ƃ����肷��ƁA�G���[�ɂȂ�B

        # y <- 5;
        > Line 1, char 0-5 : unbound identifier y.
        # x <- "hello";
        > Line 1, char 5-11 : 
          Expression has type string where int was expected.

  "unbound identifier" �� y �ƌ������O�̕ϐ������݂��Ȃ��Ƃ����Ӗ����B
  ��ڂ̃G���[�͕ϐ� x �̌^�� int (����)�Ȃ̂ɁA�� "hello" �̌^�� 
  string (������)�������̂ŁA�V�����l�����鎖���ł��Ȃ������Ƃ�����
  �����B

  �ǂ�����悭����ԈႢ�ŁA����"Expression has type ... where ... was
  expected." �Ƃ����`�̃G���[�͑����̃v���O�����̊ԈႢ���w�E���Ă���
  ��B����𐳂����������邱�Ƃ��d�v���B

e) �^�̒�`
  �g���̌^�����ɁA�V�����^���`���邱�Ƃ��ł���B���̐����͎��߂܂ŁB

f) �t�@�C������v���O������ǂݍ���
  �Ō�ɁA���̓��[�v�͒�`����͂���B��̕��@�ł͂Ȃ��B�t�@�C�����炻
  ����ǂݍ��ނ��Ƃ��ł���B���̂Ƃ��A���̓��[�v�œ��͂��ꂽ�Ƃ��ƑS
  ����������������B

  �t�@�C�� test.mal �̒��g�͎��̒ʂ肾�Ƃ���B

        fun double x = x * 2;           (* double �͈����̓�{���v�Z���� *)
        val y = 10;                     (* y ��K���Ȓl�� *)
        y + double y;                   (* ����ŎO�{���I *)

  �t�@�C���̒��� (* �� *) �ň͂܂ꂽ�����͒��߂ŁA���������B

  test.mal ��ǂݍ��ށB

        # use"test";
        val double : int -> int = <fun>
        val y : int = 10
        - : int = 30
        - : unit = ()

  �ŏ��̎O�̓��́A�ǂݍ��񂾓��͂ɂ����̂��B�Ō�� "- : unit = ()"
  �� use ���̂̌��ʂ��Buse ������ɏI���������Ƃ�\���B

2. �l�A���s�Ɛ���\��

a) ��{�f�[�^�^
  Minimal �ł͗l�X�ȃf�[�^�����̂܂܈�����B�萔�Ȃ̂ŁA���s�̌��ʂ͂�
  �̒l���̂ɂȂ�B

  * ����(int) 565 -6327 �ȂǁB
    �B���ȂƂ�������(-23)�̗l�Ɋ��ʂ�t���Ȃ���΂Ȃ�Ȃ��B

  * ����(float) 1. -5.3 2e4 �ȂǁB
    �����Ƌ�ʂ��邽�߂ɕK�� "." �� "e" ���Ȃ���΂Ȃ�Ȃ��B

  * ����(char) 'a' '\n' '\027' �ȂǁB
    �Ō�̌`��ASCII�R�[�h���O���̏\�i���ŕ\���B

  * ������(string) "hello" "April 26, 1971" �ȂǁB
    �����Ɠ��l�A�����R�[�h���g����B�����I�ɂ͔z��Ȃ̂ŁA�z��Ɋւ���
    �֐��͕�����ɂ��g����B
    �� Minimal�͕����̕����R�[�h���T�|�[�g���ē���B���ϐ�
    MINIMAL_LANG�ALC_ALL�ALANG�܂���LC_CTYPE�̌�������āASJIS�AEUC�A
    UTF8�܂���NOCONV�ɐݒ肳���B�ǂ̕ϐ����ݒ肳��Ă��Ȃ��ꍇ��SJIS
    �ɂȂ�B

  * �^�U�l(bool) true(�^) �� false(�U) �̂݁B

  * �P��(unit) �Ӗ��̂Ȃ��^�B�����Ԃ������Ȃ��Ƃ��Ɏg���B() �̂݁B

b) �萔��
  �萔�����łł������B�v�Z�͗v��Ȃ��B

  ��L�̊�{�f�[�^�^�����ɁA���̑g�����ȂǂŒl������B
  �g���̑g�������@�͎O����B

  * �g (�l1 , ... , �ln) �Ə����B�l�̌^�͂΂�΂�ł��\��Ȃ��B
    ���̌^�͗v�f�̌^��S�Ĕ��f���A�^1 * ... * �^n �ɂȂ�B
        # (1, 1.0, "one");
        - : int * float * string = (1, 1.0, "one")

  * �z��(array) [| �l1 , ... , �ln |] �Ə����B
    �^�͊F�����łȂ���΂Ȃ�Ȃ��B�v�f�̌^�� t ��������^�� t array ��
    �Ȃ�B
        # [|1, 2, 3|];
        - : int array = [|1, 2, 3|]
    �z��̓��ʂΏꍇ�Ƃ��āAstring �� char array �ɓ���B

  * ���X�g(list) [�l1 , ... , �ln] �Ə����B
    �z��Ɠ��l�A�^�͊F�����ł���B���X�g�̌^�� t list �ɂȂ�B
        # [1, 2, 3];
        - : int list = [1, 2, 3]
    �������A�z��ƈ���āA�v�f�ƃ��X�g����A���̗v�f��擪�ɉ��������X
    �g�͌v�Z�Ȃ��ɍ���(����̌����͌v�Z���v��)�B
        # 1 :: [2,3];
        - : int list = [1, 2, 3]
    �����Ɛ����������ƁA[...]���g�����������͕֋X�̂��߂ɂ��邾���ŁA
    ���X�g�͑S�� :: (cons�\���q) �� [] (�󃊃X�g) �������B
        # 1 :: 2 :: 3 :: [];
        - : int list = [1, 2, 3]

c) �v�Z��
  �֐��≉�Z�q�łł������B�萔�����܂ށB

  ��
        2 * (3 + 5)
        4. +. sin 1.5
        cos (1.3 +. 4.5)
        sub array 3 5

  �D�揇�ʂŊ֐����ł������̂ŁA���̒��Ŋ��ʂ�t���Ȃ��Ă������B
  ������ȏ�̊֐����������ׂď��������ł����B
        
  ���Z�q�Ƃ��̌^�͉��L�̂���
  * ���l���Z�q
        + - * / mod     int -> int -> int
        +. -. *. /. **  float -> float -> float 
        -               int -> int
        -.              float -> float
    ���l���Z�q�͐����p�Ǝ����p���ʁX�ɒ�`����Ă���B�������A�����̌^
    ���������Ɠ��͎��ɕ�����΁A�����p�̂��͎̂����I�Ɏ����p�ɕϊ�����
    ��B
  * ��r���Z�q
        =  <>  <  > <= >=       'a -> 'a -> bool
        == !=                   'a -> 'a -> bool
    �^�� 'a �͂ǂ̒l�ł��g����Ƃ����Ӗ����B�����^�̒l�Ȃ�ǂ̒l�ł���
    �r�ł���B��s�ڂ͒l�̃�������̕����I�Ȉʒu���r����B
  * �^�U���Z�q
        &  or           bool -> bool -> bool
    �u��1 & ��2�v�͎�1�̌��ʂ��U�������玮2�����s���Ȃ��B
    �u��1 or ��2�v�͎�1�̌��ʂ��^�������玮2�����s���Ȃ��B
  * �r�b�g���Z�q
        land lor lxor lsl lsr   int -> int -> int
    �r�b�g���Ƃ̉��Z��񋟂��Ă���B32�r�b�g�}�V���ł�int�̃r�b�g����
    32�ł���B
  * �������Z�q
        @               'a list -> 'a list -> 'a list
        ^               'a array -> 'a array -> 'a array
    ^ �͕�����ɂ��g����B�Ⴆ�΁A"hello" ^ " world" �� "hello world" 
    �ɂȂ�B
  * �z�񉉎Z�q
        �z��.[�Y��]             'a array -> int -> 'a
        �z��.[�Y��] <- �l       'a array -> int -> 'a -> unit
    �ua.[i]�v�Ŕz�� a �� i �Ԗ�(0����)�̗v�f�����o���B
    �ua.[i] <- ���v�Ŕz�� a �� i �Ԗڂ̗v�f�����̌��ʂɏ�������B

d) ��`
  ���ɒ�`�̂�肩��������������A�����ƌ`���I�ɐ�������ƁA���������`
  �̒�`���ł���B

        val �萔�� = �v�Z��
        fun �֐��� ����1 ����2 ... ����n = �v�Z��
        var �ϐ��� = �v�Z��
  
  val �� var �̏ꍇ�A���̌��ʂ̌^�����̂܂ܒl��ϐ��̌^�ɂȂ邪�Afun 
  ���Ɗ֐��ɂ͈����̌^���܂񂾊֐��^���t������B
  ��L�̒�`�ň����̌^���^1 �c �^n�Ō��ʂ̌^���^0���Ƃ���ƁA�֐��̌^
  �͂����Ȃ�

        �^1 -> �^2 -> ... -> �^n -> �^0

  ���w�ł͂��������悤�ȁA��󂪈�t�������^�͂��܂�g��Ȃ����A�v����
  �� (�^1 �~ �^2 �~ �c �~ �^n) �� �^0 �Ɠ����悤�Ȃ��̂��Ǝv���΂����B

  val�Afun�Avar �Ƃ��A�����ɕ����̒�`���ł���B���̂Ƃ��Aand ���g���B

        # val x = 3 and y = 2*2;
        val x : int = 3
        val y : int = 4

  ";"����͂����ɕ����̒�`�𓯎��ɓ��͂��邱�Ƃ��ł���B�Ӗ��͋�؂�
  �ꂽ���̂ƑS�������ł���(�O�ɏo�Ă����`���g����)���A��C�Ɍv�Z���s
  ����B

        # val x = 3
          val y = x+1;
        val x : int = 3
        val y : int = 4

e) ����
  * �I��
        if �v�Z��1 then �v�Z��2 else �v�Z��3
        if �v�Z��1 then �v�Z��2
    �v�Z��1 �����s���A���̌��ʂ� true ��������v�Z��2�����s���A���̌�
    �ʂ�Ԃ��B�����łȂ���Όv�Z��3�����s���A���̌��ʂ�Ԃ��B�v�Z��3��
    �Ȃ��ꍇ�A�v�Z��2��()��Ԃ��Ȃ���΂Ȃ�Ȃ��B

  * �����t�����[�v
        while �v�Z��1 do �v�Z��2
    �v�Z��1��true��Ԃ�����A�v�Z��2�����s����B�v�Z��2�̕Ԃ��l�Ɗ֌W
    �Ȃ��A�I����()��Ԃ��B

  * �Y���t�����[�v������
        for �ϐ��� = �v�Z��1 to �v�Z��2 do �v�Z��3
        for �ϐ��� = �v�Z��1 downto �v�Z��2 do �v�Z��3
    �v�Z��1�̌��ʂ���v�Z��2�̌��ʂ܂ł̐����̒l��ϐ��ɓ���A�v�Z��3
    �����s����Bto�̂Ƃ��͏��Adownto�̂Ƃ��͉���B

f) �u���b�N�\��
  ��`�␧��\���̒��ŁA�E�ӂɏ�����͈̂�ʓI�ȃv���O�����ł͂Ȃ��A�v
  �Z���݂̂ƂȂ��Ă���B

  �v�Z���̒��ɒ�`��������A�A�����ĕ����̌v�Z�������s�����肵�����Ƃ��A 
  �u���b�N�����Ȃ���΂Ȃ�Ȃ��B�u���b�N�� begin �Ŏn�܂�Aend �ŏI
  ���B���̒��ɁA";" �ŋ�؂�����`��v�Z����������B(��`��end�̑O��
  ��";"���ȗ����Ă�����)

  �u���b�N�̌��ʂ͍Ō�̎��̌��ʂɂȂ�B��`�ŏI���Ƃ��A()��Ԃ��B

        # fun maxabs x y =
          begin
            val x' = if x < 0 then -x else x
            and y' = if y < 0 then -y else y;
            if x' < y' then y' else x'
          end;
        val maxabs : int -> int -> int = <fun>
        # fun minmax array =
          begin
            var max = array.[0];
            var min = array.[0];
            for i = 1 to length array - 1 do
              begin
                if array.[i] > max then max <- array.[i];
                if array.[i] < min then min <- array.[i];
              end;
            (min,max)
          end;
        val minmax : 'a array -> 'a * 'a = <fun>

  maxabs �� x �� y �̐�Βl���v�Z���A�傫������Ԃ��B
  minmax �͔z��̒��̍ő�l�ƍŏ��l���v�Z���A���̑΂�Ԃ��B

g) �p�^�[���E�}�b�`���O
  ��L�� minmax �͑΂�Ԃ����A�΂���l���o���̂Ƀp�^�[���E�}�b�`���O��
  �K�v���B

        # val (mn,mx) = minmax [|2,1,4,3|];
        val mn : int = 1
        val mx : int = 4

  �������Afun��var�ƈႢ�Aval�ɂ��������֗��ȋ@�\���t���Ă����̂��B
  ���́Aval�ɂ���`�͂����Ǝ��R���B

        val �p�^�[�� = �v�Z��

  �p�^�[���͌v�Z���Ɠ��������������邪�A

  * �֐��▽�߁A���s�����悤�Ȃ��͓̂���Ȃ�

  * �ϐ��͉E�ӂ̌v�Z���ɂ���Ē�`�����B���������̕ϐ��͊��ɒ�`����
    �Ă��Ă��A���̒l�����������B

        # val (1,x) = (1,3);
        val x : int = 3

  �p�^�[���ƒl������Ȃ��Ƃ��A�G���[���N����B

        # val (1,x) = (2,3);
        > Match failure in toplevel input.

  ���̃G���[���E���āA�ꍇ�������ł���B

        # case (2,3) of (1,x) => x | (2,x) => x + 2 end;
        - : int = 5

  case���ł́A�l���ɗ^���A���̎��Ƀp�^�[���̃��X�g�Ɗe�ꍇ�ɉ����Ď�
  �s�����v�Z���̗�������B�u���b�N�Ɠ��l�A���ʂ͑I�΂ꂽ�ꍇ�̍Ō��
  ���̕Ԃ�l�ł���B

        case �v�Z�� of
          �p�^�[�� =>
            �v�Z�� ; ... ; �v�Z��
        | �p�^�[�� =>
            �v�Z�� ; ... ; �v�Z��
        | ...
        end

  �����Ō����͕̂ϐ��A�P���Ȓl�A�����Ă��̑g�̃p�^�[�����������A�V����
  �f�[�^�^���`����ƁA�������p�^�[���ɂ��g����B

h) �V�����f�[�^�^�̒�`

  �O��ނ̒�`���ł���

  1) ���̂̒�`
    �f�[�^�\����V������`����̂ł͂Ȃ��A���ɒ�`���ꂽ�f�[�^�\���ɖ�
    �O��t����BC�����typedef�ɓ���B

        # type complex == float * float;
        type complex defined.

    �^���_�ł͗��̂������I�ɓ���Ȃ��̂ŁA��ŏ����Ȃ���΂Ȃ�Ȃ��B

        # fun add_complex ((x,y) : complex) ((x',y') : complex) : complex =
                (x+x',y+y');
        val add_complex : complex -> complex -> complex = <fun>
        # add_complex (1.,2.) (3.,4.);
        - : complex = (4.0, 6.0)

    string �� char array �̗��̂����A���̏ꍇ�����͎����I�ɒu��������
    ���B

  2) ���a�^�̒�`
    �l�X�Ȏ�ނ̓��e��������ł���B

    �Ⴆ�΁A�g�����v�B�܂��F���`����B
        # type color = Diamond | Heart | Spike | Clove;
        type color defined.
    �e�\���q�͒l�Ƃ��Ă��g����B
        # Heart;
        - : color = Heart
    ����ɃJ�[�h���`����B
        # type card = Normal of color * int | Joker;
        type card defined.
    of �̌�ɍ\���q�̈�����������B
        # Normal (Clove,11);
        - : card = Normal (Clove, 11)
        # Joker;
        - : card = Joker

    ���X�g�����a�^�Ƃ��Ē�`����Ă���B:: �� [] �͓��ʂȋL���Ȃ̂ŁA
    �V�������X�g���`���悤�Ƃ���ƁA�ʂ̖��O���g���B
        # type 'a list = Cons of 'a * 'a list | Nil;
        type list defined.
    ��̗�ƈႢ�A���X�g�͌^���g������('a)�����B�l�X�ȕ��̃��X�g����
    �邩�炾�B����ɁACons �̓�Ԗڂ̈��������X�g�ł���B���X�g�͍ċA
    �I�Ȍ^�ŁACons�������������āA�Ō��Nil�ŏI���Ƃ����`�ɂȂ�B
        # Cons(1, Cons(2, Cons (3, Nil)));
        - : int list = Cons (1, Cons (2, Cons (3, Nil)))
    ���a�^�̓p�^�[���}�b�`���O�ɂ��g����B����̓��X�g�̒������v�Z����
    ���̂��B
        # fun length_list l =
            case l of
              Nil => 0
            | Cons (a,l) => 1 + length_list l
            end;
        val length_list : 'a list -> int = <fun>

    ���X�g�ł͌^������ 'a �Ə��������A�����������̈������K�v�ł���΁A
    type ('a,'b,'c) t = ... �Ƃ����`�ł�������B���a�^�����łȂ��A�^��
    ���͗��̌^�⎟�̒��ό^�ł��g����B

  3) ���ό^
    �g�̗v�f�ɖ��O��t����ƕ֗��ɂȂ�B������\�ɂ���̂́A���̒���
    �^�ł���B

    ���f���̗�𒼐ό^�ŏ����Ƃ����Ȃ�B
        # type complex = {x : float, y : float};
        type complex defined.
        # val i = {x=0.0,y=1.0};
        val i : complex = {x=0.0, y=1.0}
        # i.y;
        - : float = 1.0
        # fun add_complex a b = {x = a.x + b.x, y = a.y + b.y};
        val add_complex : complex -> complex -> complex = <fun>
        # add_complex i i;
        - : complex = {x=0.0, y=2.0}

    ���ό^�̂�����̓����́A����v�f���ςɂł��邱�Ƃ��B
        # type person = {name : string, mutable age : int};
        type person defined.
        # val me = {name = "Gariko", age = 25};
        val me : person = {name="Gariko", age=25}
        # me.age <- me.age + 1;
        - : unit = ()
        # me;
        - : person = {name="Gariko", age=26}
    ���������ςȒ��ό^�̒l�́A�ϐ��ƈႢ�A�ォ���`���ꂽ�֐��̒���
    �g������A�n������ł���B
        # fun birthday pers = pers.age <- pers.age + 1;
        val birthday : person -> unit = <fun>
        # birthday me;
        - : unit = ()
        # me;
        - : person = {name="Gariko", age=27}

3. �g���֐�
  �g���̃f�[�^�^�ɑ΂��ėl�X�Ȋ֐�����`����Ă���B

a) �z��
        length          'a array -> int
        array           int -> 'a -> 'a array
  �uarray n a�v�͒la�ŏ��������ꂽ�z������B
        copy            'a array -> 'a array
  �ucopy arr�v�͔z��arr�̃R�s�[��Ԃ��B(�R�s�[�̕ύX�͌��̔z���ς���
  ��)
        sub             'a array -> int -> int -> 'a array
  �usub arr pos len�v�͔z��arr��pos����̒���len�̕����z���Ԃ��B
        map_array       ('a -> 'b) -> 'a array -> 'b array
  �umap_array f arr�v�͊֐�f��z��arr�̑S�Ă̗v�f�ɓK�p���A���ʂ̔z��
  ��Ԃ��B
        do_array        ('a -> 'b) -> 'a array -> unit
  �umap_array�v�Ɠ��������A���ʂ͕Ԃ��Ȃ��B

b) ���X�g
        map_list        ('a -> 'b) -> 'a list -> 'b list
        do_list         ('a -> 'b) -> 'a list -> unit
  �z��Ɠ�����������X�g�ɑ΂��čs���B

c) �ϊ�
        array_of_list   'a list -> 'a array
        list_of_array   'a array -> 'a list

        string_of_int   int -> string
        int_of_string   string -> int
        string_of_float float -> string
        float_of_string string -> float

        char            int -> char
        code            char -> int

        float           int -> float
        round trunc     float -> int

        format_float    int -> bool -> float -> string
                �uformat_float prec exp x�v�� x �𕶎���ɕϊ�����B
                prec �����̐����Ȃ�A�����_�ȉ��� prec �ɌŒ肳���B
                exp �� true �Ȃ�A�w���\�����g����B

d) ���o��
        print_string    string -> unit
        print_int       int -> unit
        print_float     float -> unit
                �����̒l��\������
        newline         unit -> unit
                �unewline ()�v�͏o�͂ɉ��s��������B
        write_file      string -> string list -> unit
                �uwrite_file ���O �s�v�̓t�@�C�����O�̒��ɗ^����ꂽ�s
                �̕������������ށB

        read_string     unit -> string
        read_int        unit -> int
        read_float      unit -> float
                ������E�����E���������ꂼ����͂���B
        read_file       string -> string list
                �t�@�C���̒��g���s�̃��X�g�Ƃ��ēǂݍ��ށB

e) ���l�֐�
        not             bool -> bool
                �^�U�l�̔ے�
        maxint minint   int
                �萔�F1073741823 �� -1073741824
        exp log sqrt sin cos tan asin acos atan abs
                        float -> float
                �w���ƎO�p�֐�
        random_init     int -> unit
        random_int      int -> int
        random_float    float -> float
                �[�������̐���

f) �V�X�e�����̑�
  Minimal���I��������
        quit            unit -> unit
  �v���O������ǂݍ���
        use             string -> unit
                �uuse �t�@�C�����v�Łu�t�@�C����.mal�v��ǂݍ��ށB
        require         string -> unit
                �܂��ǂ܂�Ă��Ȃ��ꍇ�ɂ����ǂݍ��ށB
        cd              string -> unit
                �w�肳�ꂽ�f�B���N�g��(�܂��̓t�H���_)�Ɉړ�����B
  ��O
        raise           string -> 'a
                �uraise ���b�Z�[�W�v�̓��b�Z�[�W��\�����ăv���O������
                �I��������B
  �f�o�b�O
        trace           string -> unit
                �utrace f�v�̓g�b�v���x���Œ�`���ꂽ�֐�f�̌Ăяo����
                �\������B
        tracen          int -> string -> unit
                �utracen n f�v�͊֐�f��n�ȏ�̈����ɓK�p�����S�Ă̌�
                �яo����\������B�֐�f�̌^�� t1 -> .. tn -> t ������
                ��utrace f�v�́utrace n f�v�ɓ���B
        untrace         string -> unit
        untrace_all     unit -> unit
                �Ăяo���̕\�����~�߂�B
  OS�֌W
        system          string -> int
                OS�̃R�}���h�����s���A�I���R�[�h��Ԃ��B
        time            unit -> float
                ���v���Z�X�̎��s���Ԃ�b�P�ʂŕԂ��܂��B

g) �O���t�B�b�N�X�g��
  ��) MacOSX�łł͂��̊g����Apple�񋟂�X11�𗘗p���Ă��܂��B
      xterm�Ȃǂ���minimal-graph���N�����ĉ������B

  ���
        open_graph      unit -> unit
        clear_graph     unit -> unit
        close_graph     unit -> unit
                �O���t�B�b�N�X��ʂ�������A�����A����B
        size_x size_y   unit -> int
                �O���t�B�b�N�X��ʂ̕��ƍ����B
  �F
        set_color       color -> unit
                ���ꂩ��g���F��ݒ肷��B
        rgb             int -> int -> int -> color
                24�r�b�gRGB���f���ŐF���`����B
        black white red green blue yellow cyan magenta          color
                �g���̐F�B
        point_color     int -> int -> color
                �upoint_color x y�v�͍��Wx,y�̃s�N�Z���̐F��Ԃ��B
  �`��
        plot            int -> int -> unit
                �uplot x y�v�͍��Wx,y�̃s�N�Z���̐F��ݒ�̐F�ɕς���B
                ���݈ʒu�������Ɉڂ����B
        moveto          int -> int -> unit
                �umoveto x y�v�͌��݈ʒu��ݒ肷��B
        current_point   unit -> int * int
                ���݈ʒu�̍��W��Ԃ��B
        set_line_width  int -> unit
                ���̕���ݒ肷��B
        lineto          int -> int -> unit
                �ulineto x y�v�͌��݈ʒu����w��̃s�N�Z���܂Ő��������B 
                ���݈ʒu�������Ɉڂ����B
        fill_rect       int -> int -> int -> int -> unit
                �ufill_rect x y w h�v�͐ݒ�̐F�œh��ׂ��ꂽ�l�p����
                �Wx,y���畝w�ƍ���h�ŕ`���B
        set_font        string -> unit
        set_font_size   int -> unit
                ���̂̎w��B
        draw_string     string -> unit
                ����������݈ʒu�ɏ����B
  ���o��
        read_point      unit -> int * int
                �}�E�X���g���āA�w�肳�ꂽ�_�̍��W��ǂݍ��ށB
        key_pressed     unit -> bool
                �L�[��������Ă��邩�ǂ���������B
        read_key        unit -> char
                �����ꂽ�L�[�̕�����ǂށB
        sound           int -> int -> unit
                �usound f t�v�͎��g��f��t/1000�b�ԏo���B

$Id: ReadmeJP.txt,v 1.5 2004/09/24 06:35:21 garrigue Exp $
